<script>
export default {
  name: "Socials",
};
</script>

<template>
  <div class="flex align-center">
    <div class="uppercase"><a href="">Follow Us</a></div>
    <ul class="flex">
      <li>
        <a href=""><img src="../assets/img/footer-facebook.png" alt="" /></a>
      </li>
      <li>
        <a href=""><img src="../assets/img/footer-periscope.png" alt="" /></a>
      </li>
      <li>
        <a href=""><img src="../assets/img/footer-pinterest.png" alt="" /></a>
      </li>
      <li>
        <a href=""><img src="../assets/img/footer-twitter.png" alt="" /></a>
      </li>
      <li>
        <a href=""><img src="../assets/img/footer-youtube.png" alt="" /></a>
      </li>
    </ul>
  </div>
</template>

<style scoped lang="scss">
@use "../assets/scss/partials/variables.scss" as *;

a {
  margin-right: 20px;
  font-weight: bold;
  color: $blue-primary;
}
li {
  a {
    margin-right: 15px;
  }
}
</style>
