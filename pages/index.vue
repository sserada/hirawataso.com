<template>
  <section>
    <Header />
    <MainVidual />
    <About />
  </section>
</template>

<script lang="ts">
import Vue from "vue";
import About from "~/components/About.vue";
import Header from "~/components/Header.vue";
import MainVidual from "~/components/MainVisual.vue";

export default Vue.extend({
  name: "Index",
  components: {
    Header,
    MainVidual,
    About,
  }
});
</script>
