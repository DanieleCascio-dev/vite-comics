<script>
export default {
  data() {
    return {
      dcComics: [
        "Characters",
        "comics",
        "Movies",
        "TV",
        "Games",
        "Videos",
        "News",
      ],
      shop: ["Shop DC", "Shop DC Collectables"],
      DC: [
        "Terms of use",
        "Privacy policy(New)",
        "Ad Choice",
        "Advertising",
        "Jobs",
        "Subscriptions",
        "Talent Workshops",
        "CPSC Certificates",
        "Ratings",
        "Shop Help",
        "Contact Us",
      ],
      sites: ["DC", "MAD Magazine", "DC Kids", "DC Universe", "DC Power Visa"],
    };
  },
};
</script>

<template>
  <footer>
    <div class="footer-top">
      <div class="container">
        <div class="list-footer">
          <div class="logo-dc">
            <img src="../img/dc-logo-bg.png" alt="" />
          </div>
          <div class="list">
            <h2>DC COMICS</h2>
            <ul>
              <li v-for="title in dcComics">
                <a href="">{{ title }}</a>
              </li>
            </ul>
            <h2>SHOP</h2>
            <ul>
              <li v-for="elements in shop">
                <a href="">{{ elements }}</a>
              </li>
            </ul>
          </div>
          <div class="list">
            <h2>DC</h2>
            <ul>
              <li v-for="link in DC">
                <a href="">{{ link }}</a>
              </li>
            </ul>
          </div>
          <div class="list">
            <h2>SITES</h2>
            <ul>
              <li v-for="site in sites">
                <a href="">{{ site }}</a>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
    <div class="footer-bottom"></div>
  </footer>
</template>

<style lang="scss" scoped>
@use "../style/partials/variables" as *;
footer {
  height: 260px;

  .footer-top {
    height: 210px;
    background-image: url(../img/footer-bg.jpg);
    background-position: top;
    background-size: cover;
    padding: 1rem;
    position: relative;

    .list-footer {
      display: flex;
      justify-content: flex-start;

      font-size: 0.6rem;
      gap: 1.5rem;
      h2 {
        color: $char-white;
        padding-bottom: 0.5rem;
        font-size: 0.8rem;
      }
      ul {
        color: lighten($char-color, 20%);
        list-style: none;
        margin-bottom: 1rem;
        li {
          margin-bottom: 0.1rem;
          a {
            text-decoration: none;
            color: inherit;
          }
        }
      }
    }

    .logo-dc {
      position: absolute;
      right: 70px;
      top: -20px;
      z-index: 1;
      img {
        height: 250px;
      }
    }
  }

  .footer-bottom {
    height: 50px;
    background-color: $char-color;
    z-index: 2;
    position: relative;
  }
}
</style>
