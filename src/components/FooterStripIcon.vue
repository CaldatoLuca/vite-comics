<script>
export default {
  name: "StripIcon",
  data() {
    return {
      icons: [
        {
          name: "Digital Comics",
          src: "../src/assets/img/buy-comics-digital-comics.png",
          alt: "digital",
        },
        {
          name: "Dc Merchandise",
          src: "../src/assets/img/buy-comics-merchandise.png",
          alt: "merchandise",
        },
        {
          name: "Subscription",
          src: "../src/assets/img/buy-comics-subscriptions.png",
          alt: "subscription",
        },
        {
          name: "Comic Shop Locator",
          src: "../src/assets/img/buy-comics-shop-locator.png",
          alt: "shop locator",
        },
        {
          name: "Dc Power Visa",
          src: "../src/assets/img/buy-dc-power-visa.svg",
          alt: "power visa",
        },
      ],
    };
  },
};
</script>

<template>
  <ul class="flex space-between">
    <li v-for="icon in icons" class="flex align-center">
      <div class="img-container">
        <img :src="icon.src" :alt="icon.alt" />
      </div>
      <a href=""> {{ icon.name }}</a>
    </li>
  </ul>
</template>

<style scoped lang="scss">
@use "../assets/scss/partials/variables.scss" as *;

.img-container {
  width: 55px;
  height: 55px;
  margin-right: 15px;
  img {
    width: 100%;
    height: 100%;
    object-fit: contain;
    display: block;
  }
}

a {
  color: white;
  text-transform: uppercase;
}
</style>
