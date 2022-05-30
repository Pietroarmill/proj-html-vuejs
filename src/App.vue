<template>
  <div id="app">
    <AppHeader :ElementTop="this.headerTopArray" :ElementBottom="this.headerBottomArray" />
    <AppMain :blogsArray="this.blogs"/>
    <AppFooter />
  </div>
</template>

<script>
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import AppHeader from './components/AppHeader.vue';

export default {
  name: 'App',
  components: {
    AppMain,
    AppFooter,
    AppHeader
  },
  data() {
    return {
      headerTopArray: ['sign in', 'about us', 'contact us', 'buy now'],
      headerBottomArray: [
        {
          name: "home",
          active: true
        },
        {
          name: "elements",
          active: false
        },
        {
          name: "features",
          active: false
        },
        {
          name: "pages",
          active: false
        },
        {
          name: "portfolio",
          active: false
        },
        {
          name: "blog",
          active: false
        },
        {
          name: "shop",
          active: false
        },
      ],
      blogs: [
        {
          title: "How To Take Better Concert Picture in 30 Seconds",
          content:"Lorem, ipsum dolor sit amet consectetur adipisicing elit. Optio blanditiis dolorem ex reprehenderit sed maiores cum",
          type: "photography",
          src: "-46",
        },
        {
          title: "Gadgets That Make Yout Smartphone Even Smarter",
          content:"Lorem, ipsum dolor sit amet consectetur adipisicing elit. Optio blanditiis dolorem ex reprehenderit sed maiores cum",
          type: "gadgets",
          src: "-47",
        },
        {
          title: "20 Top-Rated Tourist Attractions in Manhattan",
          type: "travel",
          content:"Lorem, ipsum dolor sit amet consectetur adipisicing elit. Optio blanditiis dolorem ex reprehenderit sed maiores cum",
          src: "-48",
        },
        {
          title: "The Best Way To Ride a Motorcylce",
          type: "lifestyle",
          content:"Lorem, ipsum dolor sit amet consectetur adipisicing elit. Optio blanditiis dolorem ex reprehenderit sed maiores cum",
          src: "-49",
        },
        {
          title: "5 Fun Things to Do at the Beach",
          type: "travel",
          content:"Lorem, ipsum dolor sit amet consectetur adipisicing elit. Optio blanditiis dolorem ex reprehenderit sed maiores cum",
          src: "-50",
        },
        {
          title: "Amazingly Fresh Fruit And Herb Drinks For Summer",
          type: "recipes",
          content:"Lorem, ipsum dolor sit amet consectetur adipisicing elit. Optio blanditiis dolorem ex reprehenderit sed maiores cum",
          src: "-51",
        },
      ]
    }
  }
}
</script>

<style lang="scss">
@import "./style/common.scss";
</style>
