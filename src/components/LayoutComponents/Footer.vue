<script setup>
const year = new Date().getFullYear();

const scrollToTop = () => {
    window.scrollTo({
        top: 0,
        behavior: "smooth",
    })
}
</script>

<template>
    <footer class="footer place-items-center lg:grid-cols-2 grid-cols-1 pt-8
        bg-base-100 border-t lg:text-start text-center border-base-300" aria-label="Footer del sito">
        <article class="lg:max-w-8xl lg:py-10 flex flex-col justify-center items-center 
            gap-10 lg:gap-4 lg:flex-row lg:items-start lg:justify-between">
            <div class="max-w-sm lg:px-0 px-3">
                <h2 class="lg:text-[32px] text-[24px] font-bold text-green-400 lg:mb-6 mb-4">
                    Speechful
                </h2>
                <p class="mt-3 lg:text-[18px]/6.5 text-[15.5px]/6.5 opacity-80">
                    Micro lezioni, esercizi interattivi e pronuncia guidata per portare
                    una nuova lingua nella tua routine, pochi minuti alla volta.
                </p>
            </div>

        </article>

        <nav class="flex gap-10 lg:text-[16px] text-[14.5px] lg:flex-row 
           flex-col justify-center lg:items-start items-center md:justify-end"
            aria-label="Link di navigazione nel footer">
            <div class="space-y-3">
                <p class="font-semibold uppercase tracking-wide opacity-70">
                    Prodotto
                </p>
                <a href="#about" class="link link-hover hover:text-green-400 block">Chi siamo</a>
                <a href="#features" class="link link-hover hover:text-green-400 block">Cosa puoi fare</a>
                <a href="#stats" class="link link-hover hover:text-green-400 block">I nostri numeri</a>
                <a href="#why-us" class="link link-hover hover:text-green-400 block">Perché sceglierci</a>
            </div>

            <div class="space-y-3">
                <p class="font-semibold uppercase tracking-wide opacity-70">
                    Altro
                </p>
                <a href="#final-cta" class="link link-hover hover:text-green-400 block">Inizia gratis</a>

                <a type="button" class="link link-hover hover:text-green-400 block" @click="scrollToTop">
                    Torna su
                </a>
            </div>
        </nav>

        <div class="flex lg:flex-row px-8 py-5 bg-base-300/40 flex-col border-t border-base-300 col-span-full lg:items-stretch 
            lg:justify-between justify-center items-center text-center text-[14px] opacity-70 w-full" aria-label="Project information">
            <p>
                Copyright © {{ year }} Speechful - Tutti i diritti riservati.
            </p>
            <p>
                Progetto demo creato per esercizio front-end.
            </p>
        </div>
    </footer>
</template>