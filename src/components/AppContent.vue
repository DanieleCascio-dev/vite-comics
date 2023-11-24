<script>
import AppCard from "./AppCard.vue";

export default {
  data() {
    return {
      comics: [
        {
          thumb: "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
          price: "$19.99",
          series: "Action Comics",
          type: "comic book",
        },
        {
          thumb:
            "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
          price: "$3.99",
          series: "American Vampire 1976",
          type: "comic book",
        },
        {
          thumb:
            "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560,c_limit/Aquaman-16.jpg",
          price: "$16.99",
          series: "Aquaman",
          type: "graphic novel",
        },
        {
          thumb: "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
          price: "$2.99",
          series: "Batgirl",
          type: "comic book",
        },
        {
          thumb:
            "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
          price: "$3.99",
          series: "Batman",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
          price: "$2.99",
          series: "Batman Beyond",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
          price: "$3.99",
          series: "Batman/Superman",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
          price: "$4.99",
          series: "Batman/Superman Annual",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
          price: "$5.99",
          series: "Batman: The Joker War Zone",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
          price: "$6.99",
          series: "Batman: Three Jokers",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
          price: "$4.99",
          series: "Batman: White Knight Presents: Harley Quinn",
          type: "comic book",
        },
        {
          thumb:
            "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
          price: "$16.99",
          series: "Catwoman",
          type: "graphic novel",
        },
      ],
    };
  },
  components: { AppCard },
};
</script>

<template>
  <main>
    <div class="top-content"></div>
    <div class="bottom-content">
      <div class="container">
        <div class="content">
          <div class="row">
            <div v-for="comic in comics" :key="comic.thumb" class="col">
              <AppCard :imageName="comic.thumb" :title="comic.series" />
            </div>
          </div>
          <a href="">Load More</a>
        </div>
      </div>
    </div>
  </main>
</template>

<style lang="scss" scoped>
@use "../style/partials/variables" as *;
@use "../style/partials/mixin" as *;
main {
  min-height: 600px;
  width: 100%;
  /* background-color: $bg-primary; */

  .top-content {
    min-height: 250px;
    width: 100%;
    background-image: url(../img/jumbotron.jpg);
    background-position: top;
    background-size: cover;
  }

  .bottom-content {
    background-color: $bg-primary;
    position: relative;

    &::before {
      content: "CURRENT SERIES";
      display: inline-block;
      padding: 0.5rem 1rem;
      background-color: $primary-color;
      color: $char-white;
      position: absolute;
      font-weight: bold;
      top: -16px;
      left: 130px;
    }
  }

  .container {
    display: flex;
    align-items: center;
    height: 100%;
  }

  .content {
    min-height: 350px;
    width: 100%;
    color: #fff;
    font-weight: bold;
    padding: 2rem 0;

    .row {
      @include flex(row, center, stretch, wrap);
      gap: 1rem;

      .col {
        width: calc(100% / 6 - 1rem);
      }
    }
  }
}
</style>
