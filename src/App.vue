<template>
  <div id="app">
    <vuescroll>
      <HeaderContent />
      <HomePage />
    </vuescroll>
  </div>
</template>

<script>
import HeaderContent from "./components/HeaderContent.vue";
import HomePage from "./components/HomePage.vue";

import vuescroll from "vuescroll";
export default {
  name: "App",
  components: {
    HomePage,
    HeaderContent,
    vuescroll,
  },
};
</script>

<style lang="scss">
@import "assets/styles/imports.css";
</style>
