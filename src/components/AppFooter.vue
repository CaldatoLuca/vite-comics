<script>
import FooterStrip from "./FooterStrip.vue";
import FooterLinks from "./FooterLinks.vue";
import FooterSocials from "./FooterSocials.vue";

export default {
  name: "Footer",
  components: {
    FooterStrip,
    FooterLinks,
    FooterSocials,
  },
};
</script>

<template>
  <footer>
    <footer-strip />
    <footer-links />
    <footer-socials />
  </footer>
</template>
