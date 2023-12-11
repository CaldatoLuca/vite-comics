<script>
import HeaderLogo from "./HeaderLogo.vue";
import HeaderNav from "./HeaderNav.vue";

export default {
  name: "Header",
  components: {
    HeaderLogo,
    HeaderNav,
  },
};
</script>

<template>
  <header>
    <div class="container flex space-between align-center">
      <header-logo /> <header-nav />
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
