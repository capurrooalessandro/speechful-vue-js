<script setup>
    import { ref, onMounted, onBeforeUnmount, computed } from "vue"

    const props = defineProps({
        target: { type: Number, required: true },
        duration: { type: Number, default: 1800 }, 
        prefix: { type: String, default: "" },
        suffix: { type: String, default: "" },
        decimals: { type: Number, default: 0 }
    })

    const current = ref(0)
    const el = ref(null)

    let started = false
    let startTime = 0
    let frameId = null
    let observer = null

    const animate = (timestamp) => {
        if (!startTime) startTime = timestamp
        const elapsed = timestamp - startTime

        const progress = Math.min(elapsed / props.duration, 1) 
        const eased = 1 - Math.pow(1 - progress, 2)           

        const raw = props.target * eased

        if (props.decimals > 0) {
            const factor = Math.pow(10, props.decimals)
            current.value = Math.round(raw * factor) / factor
        } else {
            current.value = Math.floor(raw)
        }

        if (progress < 1) {
            frameId = requestAnimationFrame(animate)
        }
    }

    const startAnimation = () => {
        if (started) return
        started = true
        startTime = 0
        current.value = 0
        frameId = requestAnimationFrame(animate)
    }

    onMounted(() => {
        observer = new IntersectionObserver(
            (entries) => {
                const entry = entries[0]
                if (entry.isIntersecting) {
                    startAnimation()
                    observer.disconnect()
                }
            },
            {
                threshold: 0.01,
                root: null,
                rootMargin: "0px 0px -5% 0px"
            }
        )

        if (el.value) {
            observer.observe(el.value)
        }
    })

    onBeforeUnmount(() => {
        if (observer) observer.disconnect()
        if (frameId) cancelAnimationFrame(frameId)
    })

    const formattedValue = computed(() => {
        if (props.decimals > 0) {
            return current.value.toLocaleString("it-IT", {
                minimumFractionDigits: props.decimals,
                maximumFractionDigits: props.decimals,
            })
        }
        return current.value.toLocaleString("it-IT")
    })
</script>

<template>
    <span ref="el">
        {{ prefix }}{{ formattedValue }}{{ suffix }}
    </span>
</template>