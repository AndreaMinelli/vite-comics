<script>
export default {
  name: "Main Banner",
  data() {
    return {
      bannerLinks: [
        { text: "DIGITAL COMICS", href: "#", src: "digital-comics.png" },
        { text: "DC MERCHANDISE", href: "#", src: "merchandise.png" },
        { text: "SUBSCRIPTIONS", href: "#", src: "subscriptions.png" },
        { text: "COMIC SHOP LOCATOR", href: "#", src: "shop-locator.png" },
        { text: "DC POWER VISA", href: "#", src: "power-visa.svg" },
      ],
    };
  },
  methods: {
    buildImagePath(image) {
      return new URL(
        `../../assets/img/buy-comics-${image.src}`,
        import.meta.url
      ).href;
    },
  },
};
</script>

<template>
  <div class="banner">
    <div class="container">
      <ul>
        <li v-for="link in bannerLinks" :key="link.text">
          <a :href="link.href">
            <figure>
              <img :src="buildImagePath(link)" :alt="link.text" />
            </figure>
            <p>{{ link.text }}</p>
          </a>
        </li>
      </ul>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../../assets/scss/mixin" as *;
@use "../../assets/scss/variables" as *;
.banner {
  background-color: $lightblue;
}

ul {
  @include flex-disposition("between");
  height: 100px;
  a {
    @include flex-disposition("between");
    margin: 0 5px;
  }

  figure {
    width: 30px;
    margin-right: 10px;
  }

  p {
    color: white;
    font-size: 12px;
  }
}
</style>
