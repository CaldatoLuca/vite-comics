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
    <div class="container flex space-between align-center">
      <app-logo /> <app-header-nav />
    </div>
  </header>
</template>

<style scoped lang="scss">
@use "../assets/scss/partials/variables.scss" as *;

header {
  height: $header-height;

  .container {
    @include container;
    height: 100%;
  }
}
</style>
