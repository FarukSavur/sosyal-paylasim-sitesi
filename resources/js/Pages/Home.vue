<template>
  <Layout>
    <h1>Hoşgeldin, {{ name }}</h1>
    <h1>Yaş: {{ age }}</h1>
  </Layout>
</template>

<script>
import Layout from "./Layout/Index.vue";
export default {
  components: {
    Layout,
  },
  props: {
    name: String,
    age: Number
  },
};
</script>
