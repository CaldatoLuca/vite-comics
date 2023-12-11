<script>
import FooterSocialsButton from "./FooterSocialsButton.vue";
import FooterSocialsIcon from "./FooterSocialsIcon.vue";

export default {
  name: "Footer Socials",
  components: {
    FooterSocialsButton,
    FooterSocialsIcon,
  },
};
</script>

<template>
  <section>
    <div class="container flex space-between align-center">
      <FooterSocialsButton />
      <FooterSocialsIcon />
    </div>
  </section>
</template>

<style scoped lang="scss">
@use "../assets/scss/partials/variables.scss" as *;

section {
  background-color: $grey-primary;
  padding: 30px;
  .container {
    @include container;
  }
}
</style>
