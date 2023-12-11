<script>
import FooterStripIcon from "./FooterStripIcon.vue";

export default {
  name: "FooterStrip",
  components: {
    FooterStripIcon,
  },
};
</script>

<template>
  <section>
    <div class="container">
      <FooterStripIcon />
    </div>
  </section>
</template>

<style scoped lang="scss">
@use "../assets/scss/partials/variables.scss" as *;

section {
  background-color: $blue-primary;
  padding: 50px;
  .container {
    @include container(1200px);
  }
}
</style>
