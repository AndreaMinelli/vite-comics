<script>
import FooterTop from "./footer-child/FooterTop.vue";
export default {
  name: "App Footer",
  components: { FooterTop },
};
</script>

<template>
  <footer>
    <footer-top></footer-top>
  </footer>
</template>

<style scoped>
footer {
  font-family: "Open Sans Condensed", sans-serif;
  background-image: url("../assets/img/footer-bg.jpg");
  background-repeat: no-repeat;
  /* background-position: center; */
}
</style>
