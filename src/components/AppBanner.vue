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
      return new URL(`./dir/${img}`, import.meta.url).href;
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
            <img src="../img/buy-comics-digital-comics.png" alt="" />
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

  .conatiner {
    height: 100%;
  }

  ul {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 1rem;
    height: 100%;

    li {
      display: flex;
      gap: 0.5rem;
      align-items: center;
      .logo {
        img {
          width: 30px;
        }
      }
      a {
        font-size: 0.6rem;
        text-decoration: none;
        color: $char-white;
      }
    }
  }
}
</style>
