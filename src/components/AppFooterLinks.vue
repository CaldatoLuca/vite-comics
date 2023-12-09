<script>
import FooterLinksList from "./FooterLinksList.vue";

export default {
  name: "Footer Links",
  components: { FooterLinksList },
};
components: {
  FooterLinksList;
}
</script>

<template>
  <section>
    <div class="container flex">
      <FooterLinksList />
    </div>
  </section>
</template>

<style scoped lang="scss">
@use "../scss/partials/variables.scss" as *;
@use "../scss/partials/utility.scss" as *;

section {
  background-image: url(/img/footer-bg.jpg);
  padding: 40px;
  .container {
    @include container();
  }
}
</style>
