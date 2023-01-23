<script>
export default {
  props: {
    comic: Object,
  },
};
</script>

<template>
  <figure>
    <img :src="comic.thumb" :alt="comic.series" />
  </figure>
  <p>{{ comic.series }}</p>
</template>

<style lang="scss" scoped>
.comic-card {
  padding: 10px;

  figure {
    width: 130px;
    height: 130px;
    overflow: hidden;
    cursor: pointer;
  }

  p {
    text-transform: uppercase;
    margin: 15px 0;
    font-size: 11px;
    cursor: pointer;
  }
}
</style>
