<script>
export default {
  data() {
    return {
      bannerIcon: [
        {
          img: "buy-comics-digital-comics.png",
          title: "DIGITAL COMICS",
        },
        {
          img: "buy-comics-merchandise.png",
          title: "DC MERCHANDISE",
        },
        {
          img: "buy-comics-subscriptions.png",
          title: "SUBSCRIPTION",
        },
        {
          img: "buy-comics-shop-locator.png",
          title: "COMIC SHOP LOCATOR",
        },
        {
          img: "buy-dc-power-visa.svg",
          title: "DC POWER VISA",
        },
      ],
    };
  },
  methods: {
    getImageUrl(img) {
      return new URL(`../img/${img}`, import.meta.url).href;
    },
  },
};
</script>

<template>
  <section>
    <div class="conatiner">
      <ul>
        <li v-for="element in bannerIcon" index="element.title">
          <div class="logo">
            <img :src="getImageUrl(element.img)" alt="" />
          </div>
          <a href="">{{ element.title }}</a>
        </li>
      </ul>
    </div>
  </section>
</template>

<style lang="scss" scoped>
@use "../style/partials/variables" as *;
section {
  background-color: $primary-color;
  height: 80px;
  position: relative;
  z-index: 2;

  .conatiner {
    height: 100%;
  }

  ul {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 2rem;
    height: 100%;

    li:nth-last-child(2) {
      img {
        width: 0.9rem;
      }
    }

    li {
      display: flex;
      gap: 0.5rem;
      align-items: center;
    }
    .logo {
      img {
        width: 1.2rem;
      }
    }
    a {
      font-size: 0.6rem;
      text-decoration: none;
      color: $char-white;
    }
  }
}
</style>
