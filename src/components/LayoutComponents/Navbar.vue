<script setup>

</script>

<template>
    <nav class="navbar bg-base-100 shadow-lg py-6 lg:px-8" aria-label="Primary">
        <div class="navbar-start">
            <a href="#" class="btn btn-link text-neutral-content no-underline text-[24px] hover:text-green-400">
                Speechful
            </a>
        </div>
        <div class="navbar-end">
            <ul class="menu menu-horizontal lg:flex hidden text-[16px]">
                <li class="mt-0.5">
                    <a href="#about" class="hover:text-green-400">Chi siamo</a>
                </li>
                <li class="mt-0.5">
                    <a href="#features" class="hover:text-green-400">Cosa puoi fare</a>
                </li>
                <li class="mt-0.5">
                    <a href="#stats" class="hover:text-green-400">I nostri numeri</a>
                </li>
                <li class="me-3 mt-0.5">
                    <a href="#why-us" class="hover:text-green-400">Perchè sceglierci</a>
                </li>
                <li>
                    <a type="button" class="btn btn-success hover:text-base-300 px-3">
                        Provalo gratis
                    </a>
                </li>
            </ul>
            <div class="dropdown dropdown-end lg:hidden">
                <div tabindex="0" role="button" class="btn btn-ghost">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-7 w-7" fill="none" viewBox="0 0 24 24"
                        stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                            d="M4 6h16M4 12h8m-8 6h16" />
                    </svg>
                </div>
                <ul tabindex="-1"
                    class="menu menu-md dropdown-content [&>li>*]:justify-center bg-base-200 rounded-box z-1 mt-3 w-52 p-3 shadow-lg">
                    <li class="pb-1.5">
                        <a href="#about" class="hover:text-green-400">Chi siamo</a>
                    </li>
                    <li class="pb-1.5">
                        <a href="#features" class="hover:text-green-400">Cosa puoi fare</a>
                    </li>
                    <li class="pb-1.5">
                        <a href="#stats" class="hover:text-green-400">I nostri numeri</a>
                    </li>
                    <li>
                        <a href="#why-us" class="hover:text-green-400">Perchè sceglierci</a>
                    </li>
                    <hr class="my-3">
                    <li>
                        <a type="button" class="btn btn-success hover:text-base-300">
                            Provalo gratis
                        </a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>
</template>