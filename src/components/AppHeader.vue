<script>
import AppLogo from "./AppLogo.vue";
import AppHeaderNav from "./AppHeaderNav.vue";

export default {
  name: "Header",
  components: {
    AppLogo,
    AppHeaderNav,
  },
};
</script>

<template>
  <header>
    <app-logo />
    <app-header-nav />
  </header>
</template>

<style scoped lang="scss"></style>
