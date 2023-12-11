<script>
export default {
  name: "Jumbo",
};
</script>

<template>
  <div class="jumbotron"></div>
</template>

<style scoped lang="scss">
@use "../assets/scss/partials/variables.scss" as *;

.jumbotron {
  height: 400px;
  background-image: url(../src/assets/img/jumbotron.jpg);
}
</style>
