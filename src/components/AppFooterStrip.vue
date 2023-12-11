<script>
import StripIcon from "./StripIcon.vue";

export default {
  name: "FooterStrip",
  components: {
    StripIcon,
  },
};
</script>

<template>
  <section>
    <div class="container">
      <StripIcon />
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
