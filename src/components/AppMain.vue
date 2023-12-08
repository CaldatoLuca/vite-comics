<script>
export default {
  name: "Main",
};
</script>

<template>
  <main>
    <div class="container flex align-center">
      <h2>Content goes here...</h2>
    </div>
  </main>
</template>

<style scoped lang="scss">
@use "../scss/partials/variables.scss" as *;
@use "../scss/partials/utility.scss" as *;

main {
  background-color: tomato;
  background-color: black;

  .container {
    @include container;
    color: white;
  }
}
</style>
