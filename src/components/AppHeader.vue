<script>
export default {
  data() {
    return {
      links: [
        {
          title: "CHARACTERS",
        },
        {
          title: "COMICS",
        },
        {
          title: "MOVIES",
        },
        {
          title: "TV",
        },
        {
          title: "GAMES",
        },
        {
          title: "COLLECTIBLES",
        },
        {
          title: "VIDEOS",
        },
        {
          title: "FANS",
        },
        {
          title: "NEWS",
        },
        {
          title: "SHOP",
        },
      ],
    };
  },
};
</script>

<template>
  <header class="container">
    <div class="logo">
      <img src="../img/dc-logo.png" alt="DC logo" />
    </div>
    <nav>
      <ul>
        <li v-for="link in links">
          <a href="">{{ link.title }}</a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<style lang="scss" scoped>
@use "../style/partials/variables" as *;
@use "../style/partials/mixin" as *;
header {
  @include flex(row, space-between, center);
  /* display: flex;
  justify-content: space-between;
  align-items: center; */
  height: 80px;

  .logo {
    img {
      width: 50px;
    }
  }

  nav {
    ul {
      @include flex(row, center, center);
      /* display: flex; */
      gap: 0.5rem;
      list-style: none;
      font-size: 0.6rem;
      font-weight: bolder;
      color: $char-color;
      a {
        text-decoration: none;
        color: inherit;
        display: inline-block;
        padding: 2rem 0.2rem;
        border-bottom: 3px solid transparent;
        transition: all 0.3s;

        &:hover {
          border-bottom: 3px solid $primary-color;
        }
      }
    }
  }
}
</style>
