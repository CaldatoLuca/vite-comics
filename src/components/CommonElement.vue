<script>
export default {
  props: {
    img: String,
    text: String,
  },
};
</script>
<template>
  <div class="element">
    <div class="image">
      <img :src="img" :alt="text" />
    </div>
    <div class="text">{{ text }}</div>
  </div>
</template>
<style lang="scss" scoped>
.element {
  margin: 10px;
  text-transform: uppercase;
  text-align: start;
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
</style>
