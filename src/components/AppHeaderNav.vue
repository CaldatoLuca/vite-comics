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
  <ul>
    <li v-for="li in nav">
      <a href="">{{ li.name }}</a>
    </li>
  </ul>
</template>

<style scoped lang="scss"></style>
