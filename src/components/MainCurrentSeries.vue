<script>
export default {
  name: "Current Series",
};
</script>

<template>
  <section class="current-series">
    <h2>Current Series</h2>
    <div class="container">prova</div>
  </section>
</template>

<style scoped lang="scss">
@use "../assets/scss/partials/variables.scss" as *;

.current-series {
  color: white;
  background-color: $black-secondary;
  padding: 40px 0 10px 0;
  position: relative;

  h2 {
    background-color: $blue-primary;
    display: inline-block;
    padding: 10px 15px;
    position: absolute;
    left: 15%;
    top: -20px;
    box-shadow: 0px 10px 13px -7px #000000;
  }
  .container {
    @include container;
    height: 100%;
  }
}
</style>
