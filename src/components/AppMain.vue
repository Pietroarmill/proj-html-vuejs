<template>
  <!-- MAIN -->
  <main class="main">

    <!-- Main Blogs Section -->
    <section class="main-blogs-section">
      <div class="container">
        <div class="blog-banner with-overlay" v-for="(item, index) in BlogsArray" :key="index">

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
      </div>
    </section>
    <!-- /Main Blogs Section -->

    <!-- Main Post Section -->
    <section class="main-posts-section">
      <div class="container d-flex">

        <!-- Popular Posts  -->
        <div class="col popular--+posts">
          <h5>POPULAR POSTS</h5>
          <ul>
            <AppPost v-for="(post, index) in PopPosts" :key="index" :postObj="post" />
          </ul>
        </div>
        <!-- /Popular Posts  -->

        <!-- Recent Posts  -->
        <div class="col recent-posts">
          <h5>RECENT POSTS</h5>
          <ul>
            <AppPost v-for="(post, index) in RecentPost" :key="index" :postObj="post" />
          </ul>
        </div>
        <!-- /Recent Posts  -->

        <!-- Featured -->
        <div class="col featured">
          <h5>FEATURED POSTS</h5>

          <div class="featured-post with-overlay">
            <div class="post-img">
              <img src="../assets/img/blog-66.jpg" alt="">
            </div>
            <div class="text-img">
              <span>RECIPES</span>
              <h2>Tips to Help You Quickly Prepare your Lunch</h2>
            </div>
          </div>

          <h5>FEATURED AUTHOR</h5>
          <div class="featured-author">
            <div class="img-author">
              <img src="../assets/img/avatar.jpg" alt="">
            </div>
            <div class="text-author">
              <h4>Jhon Doe</h4>
              <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Aliquid delectus at nam porro, impedit voluptatem quibusdam optio nulla.</p>
            </div>
          </div>
        </div>
        <!-- /Featured -->

      </div>
    </section>
    <!-- /Main Post Section -->

  </main>
  <!-- /MAIN -->
</template>

<script>
import AppPost from '../components/AppPost.vue'
export default {
  name: "AppMain",
  props: {
    BlogsArray: Array,
    PopPosts: Array,
    RecentPost: Array,
  },
  components: {
    AppPost
  }
}
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";

.main {
  width: 100%;

  // BLOGS SECTION
  &-blogs-section {
    background-color: #F7F7F7;
    padding: 2rem 0;

    .container {
      display: flex;
      justify-content: space-between;
      flex-wrap: wrap;
    }

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
        margin: 0 1rem 1rem 1rem;

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

      // HOVER
      &:hover .blog-content {
        display: block;
      }
    }
  }

  // POSTS SECTION
  &-posts-section {
    padding: 3rem 0;

    .container {
      display: flex;
      justify-content: space-between;
    }

    .col {
      width: calc(96% / 3);
    }

    .featured {

      .featured-post {
        position: relative;
        color: white;
        margin: 2rem 0;

        .text-img {
          position: absolute;
          left: 1rem;
          right: 1rem;
          bottom: 1rem;

          span {
            padding: .3rem .6rem;
            background-color: $brand-blog-color;
            font-size: .5rem;
          }

          h2 {
            font-size: 1rem;
            font-weight: 800;
          }
        }
      }

      .featured-author {
        display: flex;
        margin-top: 1rem;

        .img-author {
          width: 30%;
        }

        .text-author {
          padding: .5rem 1rem;
          width: 70%;

          h4 {
            margin-bottom: .5rem;
          }
          
          p {
            color: #888888;
            font-size: .8rem;
            line-height: 20px;
          }
        }
      }
    }
  }
}
</style>