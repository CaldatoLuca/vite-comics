<script>
import CommonElement from "./CommonElement.vue";
import MainButton from "./MainButton.vue";

export default {
  name: "Current Series",
  data() {
    return {
      comics: [
        {
          thumb: "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
          price: "$19.99",
          series: "Action Comics",
          type: "comic book",
        },
        {
          thumb:
            "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
          price: "$3.99",
          series: "American Vampire 1976",
          type: "comic book",
        },
        {
          thumb:
            "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
          price: "$16.99",
          series: "Aquaman",
          type: "graphic novel",
        },
        {
          thumb: "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
          price: "$2.99",
          series: "Batgirl",
          type: "comic book",
        },
        {
          thumb:
            "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
          price: "$3.99",
          series: "Batman",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
          price: "$2.99",
          series: "Batman Beyond",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
          price: "$3.99",
          series: "Batman/Superman",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
          price: "$4.99",
          series: "Batman/Superman Annual",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
          price: "$5.99",
          series: "Batman: The Joker War Zone",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
          price: "$6.99",
          series: "Batman: Three Jokers",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
          price: "$4.99",
          series: "Batman: White Knight Presents: Harley Quinn",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
          price: "$16.99",
          series: "Catwoman",
          type: "graphic novel",
        },
      ],
    };
  },
  components: {
    CommonElement,
    MainButton,
  },
};
</script>

<template>
  <section class="current-series">
    <h2>Current Series</h2>
    <div class="container">
      <div class="comics flex">
        <CommonElement
          v-for="element in comics"
          :img="element.thumb"
          :text="element.series"
        />
      </div>
      <MainButton />
    </div>
  </section>
</template>

<style scoped lang="scss">
@use "../assets/scss/partials/variables.scss" as *;

.current-series {
  color: white;
  background-color: $black-secondary;
  padding: 50px 0 30px 0;
  position: relative;
  text-align: center;

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

    .comics {
      flex-wrap: wrap;

      :deep(.element) {
        margin: 10px;
        text-transform: uppercase;
        text-align: start;
        width: calc(100% / 6 - 20px);

        .image {
          width: 100%;
          height: 250px;
          margin-bottom: 15px;
          img {
            width: 100%;
            height: 100%;
          }
        }
      }
    }
  }
}
</style>
