<script>
export default {
  name: "Nav",
  data() {
    return {
      links: [
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
  <nav>
    <ul class="flex">
      <li v-for="link in links">
        <a :href="link.link" class="flex align-center">{{ link.name }}</a>
      </li>
    </ul>
  </nav>
</template>

<style scoped lang="scss">
@use "../assets/scss/partials/variables.scss" as *;

nav {
  height: 100%;

  ul {
    height: 100%;
    gap: 35px;
    text-transform: uppercase;
    font-weight: bold;
    li {
      height: 100%;

      a {
        height: 100%;

        &:hover {
          border-bottom: 5px solid $blue-primary;
          border-top: 5px solid transparent;
          color: $blue-primary;
        }
      }
    }
  }
}
</style>
