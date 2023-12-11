<script>
export default {
  name: "Footer Links List",
};
</script>

<template>
  <div>
    <ul>
      <li><h3 class="uppercase">Dc Comics</h3></li>
      <li><a href="">Characters</a></li>
      <li><a href="">Comics</a></li>
      <li><a href="">Movies</a></li>
      <li><a href="">TV</a></li>
      <li><a href="">Games</a></li>
      <li><a href="">Videos</a></li>
      <li><a href="">News</a></li>
    </ul>
    <ul>
      <li><h3 class="uppercase">Shop</h3></li>
      <li><a href="">Shop DC</a></li>
      <li><a href="">Shop DC Collectibles</a></li>
    </ul>
  </div>
  <div>
    <ul>
      <li><h3 class="uppercase">Dc</h3></li>
      <li><a href="">Terms of Use</a></li>
      <li><a href="">Privacy policy (New)</a></li>
      <li><a href="">Ad Choices</a></li>
      <li><a href="">Advertisement</a></li>
      <li><a href="">Jobs</a></li>
      <li><a href="">Subscriptions</a></li>
      <li><a href="">Talent Workshop</a></li>
      <li><a href="">CPSC Certificates</a></li>
      <li><a href="">Ratings</a></li>
      <li><a href="">Shop Help</a></li>
      <li><a href="">Contact Us </a></li>
    </ul>
  </div>
  <div>
    <ul>
      <li><h3 class="uppercase">Sites</h3></li>
      <li><a href="">DC</a></li>
      <li><a href="">MAD Magazine</a></li>
      <li><a href="">DC Kids</a></li>
      <li><a href="">DC Universe</a></li>
      <li><a href="">DC Power Visa</a></li>
    </ul>
  </div>
</template>

<style scoped lang="scss">
@use "../assets/scss/partials/variables.scss" as *;

ul {
  color: white;
  margin-bottom: 20px;
  margin-right: 55px;
  h3 {
    font-size: 16px;
    font-weight: bold;
    margin-bottom: 20px;
  }
  a {
    color: $grey-secondary;
    margin-bottom: 10px;
  }
}
</style>
