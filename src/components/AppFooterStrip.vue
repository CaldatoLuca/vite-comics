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
  <div class="container">
    <StripIcon />
  </div>
</template>

<style scoped lang="scss">
@use "../scss/partials/variables.scss" as *;
.container {
  @include container(1200px);
}
</style>
