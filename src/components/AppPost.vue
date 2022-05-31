<template>
  <div class="post">
    <li>
      <div class="img-post">
        <img :src="require(`../assets/img/blog${postObj.img}.jpg`)" alt="">
      </div>
      <div class="text-post">
        <h4>{{ postObj.title }}</h4>
        <small>{{ postObj.date }}</small>
      </div>
    </li>
  </div>
</template>

<script>
export default {
  name: "AppPost",
  props: {
    postObj: Object,
  }
};
</script>

<style lang="scss" scoped>
.post {
  li {
    padding: .8rem 0;
    border-bottom: 1px solid #EEEEEE;
    display: flex;

    .img-post {
      width: 50px;
      margin-right: 1rem;
    }

    .text-post {
      h4 {
        font-size: .9rem;
        font-weight: 100;
      }

      small {
        font-size: .83rem;
        color: #888888;
      }
    }
  }


}
</style>