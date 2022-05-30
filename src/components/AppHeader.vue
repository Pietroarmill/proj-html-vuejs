<template>
  <!-- HEADER -->
  <header class="header">

    <!-- Header Top -->
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
    <!-- /Header Top -->

    <!-- Header Middle -->
    <div class="header-middle">
      <div class="container">
        <div class="img-logo">
          <img src="../assets/img/logo-default-slim.png" alt="">
        </div>
      </div>
    </div>
    <!-- /Header Middle -->

    <!-- Header Bottom -->
    <div class="header-bottom">
      <div class="container">
        <ul>
          <li v-for="(item, index) in ElementBottom" :key="index">
            <a href="" :class="item.active ? 'active' : ''">{{ item.name.toUpperCase() }}</a>
          </li>
        </ul>
      </div>
    </div>
    <!-- /Header Bottom -->

  </header>
  <!-- /HEADER -->
</template>

<script>
export default {
  name: "AppHeader",
  props: {
    ElementTop: Array,
    ElementBottom: Array,
  },
};
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";

.header {

  // Header Top
  &-top {
    padding: 1rem 0;
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

  // Header Middle
  &-middle {
    padding: 2rem 0;
    border-bottom: 1px solid #F7F7F7;

    .img-logo {
      width: 100px;
    }
  }

  // Header Bottom 
  &-bottom {
    padding: 1rem 0;
    ul {
      display: flex;

      li {
        margin-right: 3.6rem;

        a {
          font-size: .8rem;
          font-weight: 800;
        }
      }
    }
  }
}
</style>