<script>
export default {
  name: "Nav",
  data() {
    return {
      nav: [
        {
          name: "Characters",
          link: "",
        },
        {
          name: "Comics",
          link: "",
        },
        {
          name: "Movies",
          link: "",
        },
        {
          name: "Tv",
          link: "",
        },
        {
          name: "Games",
          link: "",
        },
        {
          name: "Collectibles",
          link: "",
        },
        {
          name: "Videos",
          link: "",
        },
        {
          name: "Fans",
          link: "",
        },
        {
          name: "News",
          link: "",
        },
        {
          name: "Shop",
          link: "",
        },
      ],
    };
  },
};
</script>

<template>
  <ul class="flex">
    <li v-for="li in nav" class="flex align-center">
      <a :href="li.link">{{ li.name }}</a>
    </li>
  </ul>
</template>

<style scoped lang="scss">
@use "../scss/partials/utility.scss" as *;
@use "../scss/partials/variables.scss" as *;

ul {
  height: 100%;
  gap: 35px;
  text-transform: uppercase;
  font-weight: bold;
  li {
    height: 100%;

    &:hover {
      border-bottom: 5px solid $blue-primary;
      border-top: 5px solid transparent;
    }
    a:hover {
      color: $blue-primary;
    }
  }
}
</style>
