<script>
export default {
  name: "Footer Top",
  data() {
    return {
      linkList: [
        {
          title: "DC COMICS",
          links: [
            { href: "#", text: "Characters" },
            { href: "#", text: "Comics" },
            { href: "#", text: "Movies" },
            { href: "#", text: "TV" },
            { href: "#", text: "Games" },
            { href: "#", text: "Videos" },
            { href: "#", text: "News" },
          ],
        },
        {
          title: "SHOP",
          links: [
            { href: "#", text: "Shop DC" },
            { href: "#", text: "Shop DC Collectibles" },
          ],
        },
        {
          title: "DC",
          links: [
            { href: "#", text: "Therme Of Use" },
            { href: "#", text: "Privacy Policy (New)" },
            { href: "#", text: "Ad Choices" },
            { href: "#", text: "Advertising" },
            { href: "#", text: "Jobs" },
            { href: "#", text: "Subscriptions" },
            { href: "#", text: "Talent Workshops" },
            { href: "#", text: "CPSC Certificates" },
            { href: "#", text: "Ratings" },
            { href: "#", text: "Shop Help" },
            { href: "#", text: "Contact Us" },
          ],
        },
        {
          title: "SITES",
          links: [
            { href: "#", text: "DC" },
            { href: "#", text: "MAD Magazine" },
            { href: "#", text: "DC Kids" },
            { href: "#", text: "DC Universe" },
            { href: "#", text: "DC Power Visa" },
          ],
        },
      ],
    };
  },
};
</script>

<template>
  <div class="footer-top">
    <div class="container row">
      <div class="footer-nav">
        <div v-for="link in linkList" :key="link.title" class="col">
          <h4>{{ link.title }}</h4>
          <ul>
            <li v-for="subLink in link.links" :key="subLink.text">
              <a :href="subLink.href"> {{ subLink.text }}</a>
            </li>
          </ul>
        </div>
      </div>
      <div class="logo-bg"></div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../../assets/scss/mixin" as *;

.footer-top {
  background-image: url("../../assets/img/footer-bg.jpg");
  background-repeat: no-repeat;
}
.row {
  @include flex-disposition("between", "stretch");

  .col {
    margin-bottom: 10px;
  }
}
.footer-nav {
  height: 300px;
  width: 40%;
  padding: 20px 0;
  display: flex;
  flex-direction: column;
  flex-wrap: wrap;

  h4 {
    color: white;
    margin: 5px 0;
  }

  li {
    height: 17px;
  }

  a {
    color: grey;
    font-size: 12px;
  }
}
.logo-bg {
  width: 50%;
  background-image: url("../../assets/img/dc-logo-bg.png");
  background-position: center;
  background-size: cover;
}
</style>
