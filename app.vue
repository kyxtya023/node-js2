<template>
  <div class="wrapper">
    <TheHeader />
    <main class="main">
      <NuxtPage />
    </main>
    <TheFooter />
  </div>
</template>

<script>
import Theheader from "./components/TheHeader.vue";
import TheFooter from "./components/TheFooter.vue";
export default {
  components: {
    Theheader,
    TheFooter,
  },
};
</script>

<style lang="scss" scoped>
@import url("https://fonts.googleapis.com/css2?family=Nunito+Sans:wght@400;600;700&family=Unbounded:wght@500;600&display=swap");
@import url("./assets/scss/main.scss");
</style>