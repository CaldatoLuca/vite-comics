<script>
import MainJumbo from "./MainJumbo.vue";
import MainCurrentSeries from "./MainCurrentSeries.vue";

export default {
  name: "Main",
  components: {
    MainJumbo,
    MainCurrentSeries,
  },
};
</script>

<template>
  <main>
    <main-jumbo />
    <main-current-series />
  </main>
</template>

<style scoped lang="scss">
@use "../assets/scss/partials/variables.scss" as *;
</style>
