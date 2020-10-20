<template>
  <div class="home">
    <Navbar />
    <Hero />
    <Flashsale />
    <Bigsale />
    <Partner />
    <Footer />
  </div>
</template>

<script>
import Navbar from "@/components/Navbar.vue";
import Hero from "@/components/Hero.vue";
import Flashsale from "@/components/Flashsale.vue";
import Bigsale from "@/components/Bigsale.vue";
import Partner from "@/components/Partner.vue";
import Footer from "@/components/Footer.vue";

export default {
  name: "Home",
  components: {
    Navbar,
    Hero,
    Flashsale,
    Bigsale,
    Partner,
    Footer,
  },
};

window.scrollTo(0, 0);
</script>
