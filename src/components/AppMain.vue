<script>
import MainBanner from "./main-child/MainBanner.vue";
export default {
  name: "App Main",
  components: {
    MainBanner,
  },
};
</script>

<template>
  <main>
    <div class="container">
      <h3>-- Content goes here --</h3>
    </div>
    <main-banner></main-banner>
  </main>
</template>

<style scoped>
main {
  background-color: black;
  color: white;
}

h3 {
  line-height: 100px;
}
</style>
