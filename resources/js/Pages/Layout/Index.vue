<template>
  <Navbar />
  <slot />
  <Footer />
</template>

<script>
import Navbar from "./Navbar.vue";
import Footer from "./Footer.vue";
export default {
  components: {
    Navbar,
    Footer,
  },
};
</script>
