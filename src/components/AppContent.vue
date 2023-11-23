<script>
export default {
  data() {
    return;
  },
};
</script>

<template>
  <main>
    <div class="container">
      <div class="content">--> Content goes here &lt--</div>
    </div>
  </main>
</template>

<style lang="scss" scoped>
@use "../style/partials/variables" as *;
main {
  height: 80px;
  width: 100%;
  background-color: $bg-primary;

  .container {
    display: flex;
    align-items: center;

    height: 100%;
  }

  .content {
    color: #fff;
    font-weight: bold;
  }
}
</style>
