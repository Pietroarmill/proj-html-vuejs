<template>
  <footer class="footer">
    <div class="container">
      <div class="post-it">Get in Touch</div>

      <!-- FOOTER TOP -->
      <div class="footer-top">

        <!-- About -->
        <div class="about big-col">
          <h5>about the blog</h5>
          <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Natus quos deleniti cumque distinctio.</p>
          <p>Vel dolores, excepturi voluptates dicta repudiandae aut illo unde neque.</p>
          <span>VIEW MORE &#10095;</span>
        </div>
        <!-- About -->

        <!-- Recent Post -->
        <div class="recent-post small-col">
          <h5>recent posts</h5>
          <div class="footer-post d-flex">
            <div class="img-post">
              <img src="../assets/img/our-office-4-square.jpg" alt="">
            </div>
            <div class="text-post">
              <h6>lorem ipsum dolor sit, consectetur aldipiscing elit.</h6>
              <small>12:53 AM Dec 19th</small>
            </div>
          </div>
          <div class="footer-post d-flex">
            <div class="img-post">
              <img src="../assets/img/our-office-5-square.jpg" alt="">
            </div>
            <div class="text-post">
              <h6>lorem ipsum dolor sit, consectetur aldipiscing elit.</h6>
              <small>12:53 AM Dec 19th</small>
            </div>
          </div>
        </div>
        <!-- /Recent Post -->

        <!-- Recent Comments -->
        <div class="recent-comments big-col">
          <h5>recent comments</h5>
          <div class="footer-comment">
            <p>
              <span class="arrow">&#10095; </span>
              <span class="author">Jhon Doe </span>
              <span>commented on </span>
              <span class="blue">lorem ipsum dolor sit amet.</span>
            </p>
            <small>12:55 AM Dec 19th</small>
          </div>
          <div class="footer-comment">
            <p>
              <span class="arrow">&#10095;</span>
              <span class="author">Jhon Doe </span>
              <span>commented on </span>
              <span class="blue">lorem ipsum dolor sit amet.</span>
            </p>
            <small>12:55 AM Dec 19th</small>
          </div>
        </div>
        <!-- /Recent Comments -->

        <!-- Categories -->
        <div class="categories small-col">
          <h5>categories</h5>
          <div class="categories-content">
            <span class="tag" v-for="(item, index) in Tags" :key="index">{{ item }}</span>
          </div>
        </div>
        <!-- /Categories -->

      </div>
      <!-- /FOOTER TOP -->
    </div>

    <!-- FOOTER BOTTOM -->
    <div class="footer-bottom">
      <div class="container">
        <div class="col left">
          <div class="logo-footer">
            <img src="../assets/img/logo-footer.png" alt="">
          </div>
          <span>&#169; Copyright 2020. All Right Reserved</span>
        </div>
        <div class="col right">
          <div>&#10095; FAQ's</div>
          <div>&#10095; Sitemap</div>
          <div>&#10095; Contact Us</div>
        </div>
      </div>
    </div>
    <!-- /FOOTER BOTTOM -->
  </footer>
</template>

<script>
export default {
  name: "AppFooter",
  props: {
    Tags: Array,
  }
}
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";
@import url('https://fonts.googleapis.com/css2?family=Lato:wght@100;300;400;700;900&family=Shadows+Into+Light&display=swap');

.footer {
  position: relative;
  background-color: #212529;

  .post-it {
    background-color: $brand-blog-color;
    font-family: 'Shadows Into Light', cursive;
    color: white;
    padding: .5rem 1rem;
    font-size: 1.4rem;
    position: absolute;
    top: -20px;
    box-shadow: -5px 7px #005580;
  }

  // FOOTER TOP
  &-top {
    padding: 5rem 0 3rem 0;
    display: flex;
    justify-content: space-between;

    .small-col {
      width: 17%;
    }

    .big-col {
      width: 28%;
    }

    h5 {
      color: white;
      text-transform: uppercase;
      font-weight: 800;
      font-size: .7rem;
    }

    // ABOUT
    .about {

      p {
        color: #888888;
        font-size: .8rem;
        margin: 1rem 0;
        line-height: 25px;
      }

      span {
        color: white;
        font-size: .6rem;
        font-weight: 800;
        cursor: pointer;
      }
    }

    // RECENT POSTS
    .recent-post {

      .footer-post {
        margin: 1rem 0;

        .img-post {
          width: 25%;

          img {
            border-radius: 50%;
          }
        }

        .text-post {
          width: 75%;
          padding-left: .5rem;

          h6 {
            color: white;
            font-weight: 100;
            margin-bottom: .3rem;
            line-height: 15px;
            color: #B7B7B7;
          }

          small {
            font-size: .6rem;
            color: #555555;
          }
        }
      }
    }

    // RECENT COMMENTS
    .recent-comments {

      .footer-comment {
        margin: 1rem 0;

        p {
          font-size: .7rem;
          color: white;
          line-height: 25px;

          .arrow {
            color: $brand-blog-color;
            margin-right: .4rem;
          }

          .author {
            font-weight: bolder;
          }

          .blue {
            color: $brand-blog-color;
            font-weight: bolder;
          }
        }

        small {
          font-size: .6rem;
          color: #555555;
        }
      }
    }

    // CATEGORIES
    .categories {
      h5 {
        margin-bottom: 1rem;
      }

      .categories-content {
        display: flex;
        flex-wrap: wrap;

        span {
          color: white;
          background-color: black;
          padding: .5rem;
          margin: .3rem;
          border-radius: 5px;
          text-transform: uppercase;
          font-size: .5rem;
          font-weight: 900;
          cursor: pointer;
        }
      }
    }
  }

  // FOOTER BOTTOM
  &-bottom {
    background-color: #1C2023;
    padding: 2rem 0;
    color: #555555;


    .container {
      display: flex;
      justify-content: space-between;
    }

    .col {
      display: flex;
      align-items: center;
    }

    .col.left {

      .logo-footer {
        width: 100px;
        margin-right: 3em;

        img {
          filter: opacity(.5);
        }
      }

      span {
        font-size: .8rem;
      }
    }

    .col.right {
      div {
        margin-left: 1rem;
        cursor: pointer;
      }
    }
  }
}
</style>