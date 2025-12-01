<script setup>
    import StatsCounter from '../StatsCounter.vue';
</script>

<template>
    <section ref="statsSectionRef" class="lg:py-26 py-18 px-4 text-center
        bg-base-100 text-shadow-lg" aria-label="Stats section">
        <header class="max-w-5xl mx-auto text-center lg:mb-10 sm:mb-14 mb-17">
            <h2 class="text-[38px] font-bold mb-3 text-green-400">
                I nostri numeri
            </h2>
        </header>

        <section class="flex lg:flex-row flex-col justify-center">
            <div class="stats stats-vertical lg:stats-horizontal shadow bg-base-200 lg:mx-auto sm:mx-14 lg:p-5 p-3 mx-3">
                <div class="stat">
                    <div class="stat-title text-[17.5px]">Studenti attivi ogni mese</div>
                    <div class="stat-value text-[40px] lg:py-1 py-2">
                        <StatsCounter :target="25" suffix="K+" />
                    </div>
                    <div class="stat-desc text-[15px]">In tutto il mondo</div>
                </div>

                <div class="stat">
                    <div class="stat-title text-[17.5px]">Lingue disponibili</div>
                    <div class="stat-value text-[40px] lg:py-1 py-2">
                        <StatsCounter :target="12" />
                    </div>
                    <div class="stat-desc text-[15px]">Nuovi corsi in arrivo</div>
                </div>

                <div class="stat">
                    <div class="stat-title text-[17.5px]">Esercizi completati</div>
                    <div class="stat-value text-[40px] lg:py-1 py-2">
                        <StatsCounter :target="1.8" suffix="M+" :decimals="1" />
                    </div>
                    <div class="stat-desc text-[15px]">Dati aggiornati ogni settimana</div>
                </div>

                <div class="stat">
                    <div class="stat-title text-[17.5px]">Valutazione media</div>
                    <div class="stat-value text-[40px] lg:py-1 py-2">
                        <StatsCounter :target="4.8" :decimals="1" />/5
                    </div>
                    <div class="stat-desc text-[15px]">Recensioni verificate</div>
                </div>
            </div>
        </section>
    </section>
</template>