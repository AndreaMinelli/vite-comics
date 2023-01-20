<script>
import FooterTop from "./footer-child/FooterTop.vue";
import FooterBottom from "./footer-child/FooterBottom.vue";
export default {
  name: "App Footer",
  components: { FooterTop, FooterBottom },
};
</script>

<template>
  <footer>
    <footer-top></footer-top>
    <footer-bottom></footer-bottom>
  </footer>
</template>

<style scoped>
footer {
  font-family: "Open Sans Condensed", sans-serif;
}
</style>
