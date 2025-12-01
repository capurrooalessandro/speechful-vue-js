<script setup>
	import Navbar from '../LayoutComponents/Navbar.vue';
    import HeroSection from '../MainPageComponents/HeroSection.vue';
    import AboutUsSection from '../MainPageComponents/AboutUsSection.vue';
    import FeaturesSection from '../MainPageComponents/FeaturesSection.vue';
    import StatsSection from '../MainPageComponents/StatsSection.vue';
    import WhyUsSection from '../MainPageComponents/WhyUsSection.vue';
    import CTASection from '../MainPageComponents/CTASection.vue';
    import Footer from '../LayoutComponents/Footer.vue';
</script>

<template>
    <Navbar class="sticky z-10 top-0"/>
    <main>
        <HeroSection />
        <AboutUsSection id="about" />
        <FeaturesSection id="features" />
        <StatsSection id="stats" />
        <WhyUsSection id="why-us" />
        <CTASection id="final-cta" />
    </main>
    <Footer />
</template>