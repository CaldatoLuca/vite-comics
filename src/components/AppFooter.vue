<script>
import AppFooterStrip from "./AppFooterStrip.vue";

export default {
  name: "Footer",
  components: {
    AppFooterStrip,
  },
};
</script>

<template>
  <footer>
    <app-footer-strip />
  </footer>
</template>

<style scoped lang="scss">
@use "../scss/partials/variables.scss" as *;

footer {
  padding: 50px 0;
  background-color: $blue-primary;
}
</style>
