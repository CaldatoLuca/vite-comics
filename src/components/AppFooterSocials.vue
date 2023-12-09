<script>
import AppButton from "./AppButton.vue";
import FooterSocials from "./FooterSocials.vue";

export default {
  name: "Footer Socials",
  components: {
    AppButton,
    FooterSocials,
  },
};
</script>

<template>
  <section>
    <div class="container flex space-between align-center">
      <AppButton />
      <FooterSocials />
    </div>
  </section>
</template>

<style scoped lang="scss">
@use "../scss/partials/variables.scss" as *;
@use "../scss/partials/utility.scss" as *;

section {
  background-color: $grey-primary;
  padding: 30px;
  .container {
    @include container;
  }
}
</style>
