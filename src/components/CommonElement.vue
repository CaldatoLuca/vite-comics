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
