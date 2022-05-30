<template>
  <header class="header">
    <div class="header-top">
      <div class="container">
        <small>Everything about Lifestyle, Travel and Gadgets!</small>
        <ul>
          <li v-for="(item, index) in ElementTop" :key="index">
            <a href="">{{ item.toUpperCase() }}</a>
          </li>
        </ul>
      </div>
    </div>
    <div class="header-middle">
      <div class="img-logo">
        <img src="../assets/img/logo-default-slim.png" alt="">
      </div>
    </div>
    <div class="header-bottom"></div>
  </header>
</template>

<script>
export default {
  name: "AppHeader",
  props: {
    ElementTop: Array,
  },
};
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";

.header {

  &-top {
    padding: 1rem;
    background-color: $brand-blog-color;
    color: white;
    font-weight: 500;

    .container {
      display: flex;
      align-items: center;
    }

    ul {
      display: flex;

      li {
        margin: 0 1rem;

        a {
          color: white;
          font-size: .8rem;
        }
      }
    }
  }
}
</style>