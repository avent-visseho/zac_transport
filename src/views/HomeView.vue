<script setup>
import SubHeader from '@/components/Header/SubHeader.vue';
import Header from '@/components/Header/Header.vue';
import Banner from '@/components/banner/Banner.vue';
import Featured from '@/components/featured/Featured.vue';
import BestDeal from '@/components/deal/BestDeal.vue';
import SlideBus from '@/components/property/SlideBus.vue';
import Gallery from '@/components/imageGallery/Gallery.vue';
import ContactSection from '@/components/banner/ContactSection.vue';
import ContactForm from '@/components/forms/ContactForm.vue';
import Footer from '@/components/footer/Footer.vue';
import ServicesCard from '@/components/services/ServicesCard.vue'
import SpeedDialog from '@/components/SpeedDialog/SpeedDialog.vue'
</script>

<template>
    <SubHeader />
    <Header />
    <Banner />
    <Featured />
    <ServicesCard />
    <Gallery />
    <!-- <BestDeal /> -->
    <!--     <SlideBus /> -->
    <ContactSection />
    <ContactForm />
    <SpeedDialog />
    <Footer />
</template>
