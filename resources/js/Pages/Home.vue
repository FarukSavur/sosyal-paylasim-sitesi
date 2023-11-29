<template>
  <Head>
    <title>Deneme Proje</title>
  </Head>
  <Layout>
    <div class="container">
      <div class="row py-4">Home</div>
    </div>
  </Layout>
</template>

<script>
import { Head } from "@inertiajs/vue3";

import Layout from "./Layout/Index.vue";
export default {
  components: {
    Layout,
    Head,
  },
  props: {},
};
</script>
