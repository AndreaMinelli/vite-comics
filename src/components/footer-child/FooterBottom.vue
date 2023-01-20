<script>
export default {
  name: "Footer Bottom",
  data() {
    return {
      socialLink: [
        { href: "#", src: "footer-facebook.png" },
        { href: "#", src: "footer-twitter.png" },
        { href: "#", src: "footer-youtube.png" },
        { href: "#", src: "footer-pinterest.png" },
        { href: "#", src: "footer-periscope.png" },
      ],
    };
  },
  methods: {
    buildImagePath(image) {
      return new URL(`../../assets/img/${image.src}`, import.meta.url).href;
    },
  },
};
</script>

<template>
  <div class="footer-bottom">
    <div class="container row">
      <button type="button">SIGN-UP NOW!</button>
      <nav class="our-social">
        <p>FOLLOW US</p>
        <ul>
          <li v-for="link in socialLink" :key="link.src">
            <a :href="link.href">
              <img :src="buildImagePath(link)" alt="" />
            </a>
          </li>
        </ul>
      </nav>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../../assets/scss/mixin" as *;
.footer-bottom {
  padding: 15px 0;
  background-color: rgb(48, 48, 48);
}

.row {
  @include flex-disposition("between");
}

.our-social {
  @include flex-disposition("between");
  p {
    margin: 0 10px;
    font-weight: bolder;
    color: dodgerblue;
    font-size: 15px;
  }
  ul {
    display: flex;
    li {
      margin: 0 10px;
      width: 30px;
    }
  }
}

button {
  background-color: transparent;
  border: 1px solid dodgerblue;
  font-weight: bold;
  color: white;
  padding: 8px 15px;
  font-size: 12px;
  cursor: pointer;
}
</style>
