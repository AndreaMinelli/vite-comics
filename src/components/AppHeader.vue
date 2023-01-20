<script>
export default {
  name: "App Header",
  data() {
    return {
      links: [
        {
          text: "Characters",
          url: "#",
          current: false,
        },
        {
          text: "Comics",
          url: "#",
          current: true,
        },
        {
          text: "Movies",
          url: "#",
          current: false,
        },
        {
          text: "TV",
          url: "#",
          current: false,
        },
        {
          text: "Games",
          url: "#",
          current: false,
        },
        {
          text: "Collectibles",
          url: "#",
          current: false,
        },
        {
          text: "Videos",
          url: "#",
          current: false,
        },
        {
          text: "Fans",
          url: "#",
          current: false,
        },
        {
          text: "News",
          url: "#",
          current: false,
        },
        {
          text: "Shop",
          url: "#",
          current: false,
        },
      ],
    };
  },
  methods: {
    isActive(link) {
      return link.current;
    },
  },
};
</script>

<template>
  <header>
    <div class="container row">
      <figure>
        <a href="#">
          <img src="../assets/img/dc-logo.png" alt="DC logo" />
        </a>
      </figure>
      <nav>
        <ul>
          <li v-for="link in links" :key="link.text">
            <a :href="link.url" :class="{ active: isActive(link) }">
              {{ link.text }}</a
            >
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<style lang="scss" scoped>
@use "../assets/scss/mixin" as *;

header {
  font-family: "Open Sans Condensed", sans-serif;

  ul {
    @include flex-disposition("between");

    a {
      display: inline-block;
      text-transform: uppercase;
      line-height: 77px;
      border-bottom: 3px solid transparent;
      margin: 0 10px;
      font-size: 12px;
      font-weight: bold;

      &.active,
      &:hover {
        border-color: dodgerblue;
        color: dodgerblue;
      }
    }
  }
  .row {
    height: 80px;
    @include flex-disposition("between");
  }

  figure {
    width: 60px;
  }
}
</style>
