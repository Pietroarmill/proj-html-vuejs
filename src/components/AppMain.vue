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
            <AppSmallPost v-for="(post, index) in PopPosts" :key="index" :postObj="post" />
          </ul>
        </div>
        <!-- /Popular Posts  -->

        <!-- Recent Posts  -->
        <div class="col recent-posts">
          <h5>RECENT POSTS</h5>
          <ul>
            <AppSmallPost v-for="(post, index) in RecentPost" :key="index" :postObj="post" />
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
              <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Aliquid delectus at nam porro, impedit
                voluptatem quibusdam optio nulla.</p>
            </div>
          </div>
        </div>
        <!-- /Featured -->

      </div>
    </section>
    <!-- /Main Post Section -->

    <!-- Row Blue -->
    <AppRowBlue :btnArray="btnRowBlue" />
    <!-- /Row Blue -->

    <section class="main-home-posts">
      <div class="container d-flex">
        <div class="posts-box">
          <AppPost v-for="(item, index) in HomePosts" :key="index" :post="item" />

          <div class="post">
            <div class="images-post">
              <img src="../assets/img/blog-13.jpg" alt="">
              <img src="../assets/img/blog-16.jpg" alt="">
              <img src="../assets/img/blog-20.jpg" alt="">
              <img src="../assets/img/blog-23.jpg" alt="">
              <img src="../assets/img/blog-29.jpg" alt="">
              <img src="../assets/img/blog-40.jpg" alt="">
            </div>
            <div class="content-post d-flex">
              <div class="date-post">
                <div class="day">8</div>
                <div class="month">JAN</div>
              </div>
              <div class="text-post">
                <h2>10 Best Travel Tips After 5 Years Traveling The World</h2>
                <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Temporibus, ullam, quod, praesentium nihil
                  cum non error doloribus quos officia est maxime corrupti! Earum suscipit doloribus recusandae maiores.
                  Iusto, unde alias?</p>
                <div class="info-post">
                  <div class="author">
                    <span>By </span>
                    <a href="">Jhon Doe</a>
                  </div>
                  <div class="type">
                    <a href="">Lifestyle, Travel</a>
                  </div>
                  <div class="comments">
                    <a href="">9 comments</a>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <div class="page-numbers">
            <div class="page-btn">&#10094;</div>
            <div class="page-btn page-active">1</div>
            <div class="page-btn">2</div>
            <div class="page-btn">3</div>
            <div class="page-btn">&#10095;</div>
          </div>
        </div>

        <div class="other-post">

          <h5>LATEST FROM TWITTER</h5>
          <div class="twitter">
            <div class="twitter-content d-flex">
              <div class="left">LO</div>
              <div class="right">
                <p>If you have any suggestion for the next updates, let us know.</p>
                <a href="">01:05 PM Sep 18th</a>
              </div>
            </div>
            <div class="twitter-content d-flex">
              <div class="left">LO</div>
              <div class="right">
                <p>We have just update Porto Admin. Check the changelog for more information</p>
                <a href="">01:04 PM Sep 18th</a>
              </div>
            </div>
          </div>

          <h5>PHOTO FROM INSTAGRAM</h5>
          <div class="insta">
            <img src="../assets/img/29739607_2020680068220520_4509928046932787200_n.jpg" alt="">
            <img src="../assets/img/30087804_253872848488989_8792603541668626432_n.jpg" alt="">
            <img src="../assets/img/29415620_196477127626244_3250318472361541632_n.jpg" alt="">
            <img src="../assets/img/30078414_1274410412703843_8290935809419247616_n.jpg" alt="">
            <img src="../assets/img/30077195_2066750973610181_3733150062893596672_n.jpg" alt="">
            <img src="../assets/img/29415304_166583630713703_1032667922171953152_n.jpg" alt="">
          </div>

          <h5>TAGS</h5>
          <div class="tags">
            <ul>
              <li>design</li>
              <li>brands</li>
              <li>video</li>
              <li>business</li>
              <li>travel</li>
            </ul>
          </div>

          <h5>FIND US ON FACEBOOK</h5>
          <div class="facebook">
            <span>
              <a href="">Okler Themes</a>
            </span>
          </div>
        </div>
      </div>
    </section>

  </main>
  <!-- /MAIN -->
</template>

<script>
import AppSmallPost from '../components/AppSmallPost.vue'
import AppRowBlue from '../components/AppRowBlue.vue'
import AppPost from '../components/AppPost.vue';
export default {
  name: "AppMain",
  props: {
    BlogsArray: Array,
    PopPosts: Array,
    RecentPost: Array,
    btnRowBlue: Array,
    HomePosts: Array,
  },
  components: {
    AppSmallPost,
    AppRowBlue,
    AppPost,
  }
}
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";

.main {
  width: 100%;
  padding-bottom: 4rem;

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

    h5 {
      font-size: .7rem;
      font-weight: 900;
    }

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
            padding: .2rem .3rem;
            background-color: $brand-blog-color;
            font-size: .4rem;
          }

          h2 {
            margin-top: .5rem;
            font-size: .8rem;
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

  &-home-posts {
    margin-top: 3rem;

    .posts-box {
      width: 75%;

      .post {

        .images-post {
          display: flex;
          flex-wrap: wrap;

          img {
            width: calc(100% / 3);
          }
        }
      }

      .page-numbers {
        display: flex;
        justify-content: flex-end;
        color: $brand-blog-color;

        .page-btn {
          border: 1px solid #F7F7F7;
          padding: .5rem .7rem;
          display: flex;
          align-items: center;
          cursor: pointer;
        }
      }
    }

    .other-post {
      width: 25%;
      padding-left: 2rem;

      h5 {
        font-size: .8rem;
        font-weight: 900;
        margin: 0 0 1rem 0;
      }

      .twitter {
        .twitter-content {
          margin-bottom: 1rem;

          .left {
            padding-right: .6rem;
            font-size: .9rem;
          }

          .right {
            color: #888888;
            font-size: .8rem;

            p {
              margin-bottom: .5rem;
            }

            a {
              color: $brand-blog-color;
            }
          }
        }
      }

      .insta {
        display: flex;
        flex-wrap: wrap;
        margin-bottom: 1rem;

        img {
          width: calc(100% / 3);
        }
      }

      .tags {
        margin-bottom: 6rem; 

        ul {
          display: flex;
          justify-content: space-between;
          flex-wrap: wrap;
          li {
            text-transform: uppercase;
            font-size: .6rem;
            font-weight: 900;
            background-color: black;
            color: white;
            padding: .1rem .4rem;
            border-radius: 10px;
          }
        }
      }

      .facebook {
        
        span {
          padding: 1rem;
          border-left: 6px solid #EEEEEE;

          a {
            color: $brand-blog-color;
          }
        }
      }
    }
  }
}
</style>