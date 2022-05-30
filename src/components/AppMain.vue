<template>
  <!-- MAIN -->
  <main class="main">
    <div class="container">

      <!-- Main Blogs Section -->
      <section class="main-blogs-section">
        <div class="blog-banner with-overlay" v-for="(item, index) in blogsArray" :key="index">

          <div class="blog-img">
            <img :src="require(`../assets/img/blog${item.src}.jpg`)" alt="">
          </div>

          <!-- text blog -->
          <div class="text-blog">
            <span class="blog-type">{{ item.type.toUpperCase() }}</span>
            <h2 class="blog-title">{{ item.title }}</h2>
            <p class="blog-content">{{ item.content }}</p>
          </div>
          <!-- /text blog -->
        </div>

      </section>
      <!-- /Main Blogs Section -->

      <!-- Main Post Section -->
      <section class="main-post-section">
      </section>
      <!-- /Main Post Section -->

    </div>
  </main>
  <!-- /MAIN -->
</template>

<script>

export default {
  name: "AppMain",
  props: {
    blogsArray: Array,
  },
  components: {

  }
}
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";

.main {
  background-color: #F7F7F7;
  width: 100%;
  padding: 2rem 0;

  &-blogs-section {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;


    .blog-banner {
      width: calc(96% / 3);
      display: flex;
      align-items: flex-end;
      color: white;
      margin: 1rem 0;
      position: relative;
      overflow: hidden;

      .text-blog {
        position: absolute;
        margin: 0 0 1rem 1rem;

        .blog-type {
          padding: .3rem .6rem;
          background-color: $brand-blog-color;
          font-size: .5rem;
        }

        .blog-title {
          font-size: 1.3rem;
          margin-top: .7rem;
        }

        .blog-content {
          display: none;
          color: #B7B7B7;
          font-weight: bold;
          line-height: 25px;
        }
      }

      &:hover .blog-content {
        display: block;
      }
    }
  }
}
</style>