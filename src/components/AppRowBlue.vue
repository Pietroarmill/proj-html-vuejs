<template>
  <div class="row-blue">
    <div class="container">
      <div class="arrow">&#10094;</div>
      <ul>
        <li v-for="(btn, index) in btnArray" :key="index" class="btn">
          <a href="">{{ btn.toUpperCase() }}</a>
        </li>
      </ul>
      <div class="arrow">&#10095;</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AppRowBlue",
  props: {
    btnArray: Array,
  }
}
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";

.row-blue {
  background-color: $brand-blog-color;
  height: 100px;

  .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 100%;
  }

  ul {
    width: 90%;
    display: flex;
    justify-content: space-around;

    .btn {
      a {
        font-size: .6rem;
        color: white;
        padding: 12px 30px;
        background-color: black;
      }
    }

  }

  .arrow {}
}
</style>