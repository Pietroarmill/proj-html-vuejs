<template>
  <div class="post">
    <div class="img-post">
      <img :src="require(`../assets/img/blog${post.img}.jpg`)" alt="">
    </div>
    <div class="content-post d-flex">
      <div class="date-post">
        <div class="day">{{ post.day }}</div>
        <div class="month">{{ post.month.toUpperCase() }}</div>
      </div>
      <div class="text-post">
        <h2>{{ post.title }}</h2>
        <p>{{ post.content }}</p>
        <div class="info-post">
          <div class="author">
            <span>By </span>
            <a href="">{{ post.author }}</a>
          </div>
          <div class="type">
            <a href="">{{ post.type }}</a>
          </div>
          <div class="comments">
            <a href="">{{ post.comments }} comments</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AppPost",
  props: {
    post: Object,
  }
}
</script>

<style lang="scss">
.post {

  .content-post {
    margin-top: 1rem;

    .date-post {
      width: 8%;
      padding-right: 2%;
      text-align: center;
      font-size: .6rem;

      .day {
        font-weight: 900;
        background-color: #F7F7F7;
        padding: 15px 0;
      }

      .month {
        background-color: black;
        color: white;
        padding: 5px 0;
      }
    }

    .text-post {
      width: 92%;
      padding-bottom: 2rem;
      margin-bottom: 2rem;
      border-bottom: 1px solid #F7F7F7;

      p {
        font-size: .9rem;
        color: #888888;
        margin: 1rem 0;
        line-height: 25px;
      }

      .info-post {
        display: flex;
        color: #888888;
        a {
          color: #0088CC;
        }
      }
    }
  }
}
</style>