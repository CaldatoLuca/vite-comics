<script>
import AppFooterStrip from "./AppFooterStrip.vue";
import AppFooterLinks from "./AppFooterLinks.vue";

export default {
  name: "Footer",
  components: {
    AppFooterStrip,
    AppFooterLinks,
  },
};
</script>

<template>
  <footer>
    <app-footer-strip />
    <app-footer-links />
  </footer>
</template>

<style scoped lang="scss">
@use "../scss/partials/variables.scss" as *;
</style>
