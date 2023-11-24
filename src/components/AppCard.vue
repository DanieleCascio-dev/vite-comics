<script>
export default {
  props: {
    imageName: String,
    title: String,
  },
};
</script>

<template>
  <div class="card">
    <img :src="imageName" alt="" />
    <h4 class="title">{{ title }}</h4>
  </div>
</template>

<style lang="scss" scoped>
@use "../style/partials/variables" as *;
.card {
  img {
    max-width: 100%;
    aspect-ratio: 1;
    object-fit: cover;
    object-position: top;
  }

  .title {
    margin-top: 0.5rem;
    font-size: 0.8rem;
    color: lighten($char-color, 50%);
  }
}
</style>
