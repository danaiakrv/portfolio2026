<template>
    <div>
        <Navbar />
        <Banner />
        <AboutSection />
        <hr class="w-1/2 mx-auto my-6 border-t border-gray-300" />
        <FrontendSection />
        <hr class="w-1/2 mx-auto my-6 border-t border-gray-300" />
        <UxUiSection />
        <hr class="w-1/2 mx-auto my-6 border-t border-gray-300" />
        <OtherSection />
        <Footer />
    </div>
</template>

<script setup>
import Navbar from '../components/Navbar.vue'
import Banner from '../components/Banner.vue'
import AboutSection from '../components/AboutSection.vue'
import FrontendSection from '../components/FrontendSection.vue'
import UxUiSection from '../components/UxUiSection.vue'
import OtherSection from '../components/OtherSection.vue'
import Footer from '../components/Footer.vue'
</script>