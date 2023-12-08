<script>
export default {
  name: "StripIcon",
  data() {
    return {
      icons: [
        {
          name: "Digital Comics",
          src: "/img/buy-comics-digital-comics.png",
          alt: "digital",
        },
        {
          name: "Dc Merchandise",
          src: "/img/buy-comics-merchandise.png",
          alt: "merchandise",
        },
        {
          name: "Subscription",
          src: "/img/buy-comics-subscriptions.png",
          alt: "subscription",
        },
        {
          name: "Comic Shop Locator",
          src: "/img/buy-comics-shop-locator.png",
          alt: "shop locator",
        },
        {
          name: "Dc Power Visa",
          src: "/img/buy-dc-power-visa.svg",
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
      <img :src="icon.src" :alt="icon.alt" />
      <a href=""> {{ icon.name }}</a>
    </li>
  </ul>
</template>

<style scoped lang="scss">
@use "../scss/partials/utility.scss" as *;

a {
  color: white;
  text-transform: uppercase;
}

img {
  width: 55px;
  margin-right: 15px;
}
</style>
