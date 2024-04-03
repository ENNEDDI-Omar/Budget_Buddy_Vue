<script>
import Navbar from '@/components/Navbar.vue';
import HomePage from '@/pages/HomePage.vue';
import ContactUs from '@/components/ContactUs.vue';
import Footer from '@/components/Footer.vue';

export default {
  components: {
    Navbar,
    HomePage,
    ContactUs,
    Footer
  }
};

</script>

<template>
  <main>
    <Navbar />
    <HomePage />
    <ContactUs />
    <Footer />
  </main>
</template>


