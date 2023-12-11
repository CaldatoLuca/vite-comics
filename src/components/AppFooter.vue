<script>
import AppFooterStrip from "./AppFooterStrip.vue";
import AppFooterLinks from "./AppFooterLinks.vue";
import AppFooterSocials from "./AppFooterSocials.vue";

export default {
  name: "Footer",
  components: {
    AppFooterStrip,
    AppFooterLinks,
    AppFooterSocials,
  },
};
</script>

<template>
  <footer>
    <app-footer-strip />
    <app-footer-links />
    <app-footer-socials />
  </footer>
</template>
