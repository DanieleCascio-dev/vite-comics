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
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding-top: 1rem;
  margin-bottom: 1rem;

  .logo {
    img {
      width: 50px;
    }
  }

  nav {
    ul {
      display: flex;
      gap: 0.5rem;
      list-style: none;
      font-size: 0.6rem;
      font-weight: bolder;
      color: $char-color;
      a {
        text-decoration: none;
        color: inherit;
        display: inline-block;
        padding: 2rem 0.5rem;

        &:hover {
          border-bottom: 3px solid $primary-color;
        }
      }
    }
  }
}
</style>
