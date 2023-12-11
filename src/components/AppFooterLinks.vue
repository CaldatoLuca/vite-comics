<script>
import FooterLinksList from "./FooterLinksList.vue";
import FooterLinksBgImage from "./FooterLinksBgImage.vue";

export default {
  name: "Footer Links",
  components: {
    FooterLinksList,
    FooterLinksBgImage,
  },
};
</script>

<template>
  <section>
    <div class="container flex">
      <FooterLinksList />
      <FooterLinksBgImage />
    </div>
  </section>
</template>

<style scoped lang="scss">
@use "../assets/scss/partials/variables.scss" as *;

section {
  background-image: url(../src/assets/img/footer-bg.jpg);
  padding: 40px;
  position: relative;
  overflow: hidden;
  .container {
    @include container();
  }
}
</style>
