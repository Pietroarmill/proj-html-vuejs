<template>
  <div id="app">
    <AppHeader :ElementTop="this.headerTopArray" :ElementBottom="this.headerBottomArray" />
    <AppMain
      :BlogsArray="this.blogs"
      :PopPosts="this.popularPost"
      :RecentPost="this.recentPost"
      :btnRowBlue="this.btnRowBlue"
      :HomePosts="this.homePosts"
    />
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
          content: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Optio blanditiis dolorem ex reprehenderit sed maiores cum",
          type: "photography",
          src: "-46",
        },
        {
          title: "Gadgets That Make Yout Smartphone Even Smarter",
          content: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Optio blanditiis dolorem ex reprehenderit sed maiores cum",
          type: "gadgets",
          src: "-47",
        },
        {
          title: "20 Top-Rated Tourist Attractions in Manhattan",
          type: "travel",
          content: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Optio blanditiis dolorem ex reprehenderit sed maiores cum",
          src: "-48",
        },
        {
          title: "The Best Way To Ride a Motorcylce",
          type: "lifestyle",
          content: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Optio blanditiis dolorem ex reprehenderit sed maiores cum",
          src: "-49",
        },
        {
          title: "5 Fun Things to Do at the Beach",
          type: "travel",
          content: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Optio blanditiis dolorem ex reprehenderit sed maiores cum",
          src: "-50",
        },
        {
          title: "Amazingly Fresh Fruit And Herb Drinks For Summer",
          type: "recipes",
          content: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Optio blanditiis dolorem ex reprehenderit sed maiores cum",
          src: "-51",
        },
      ],
      popularPost: [
        {
          img: "-55",
          title: "Simple Ways to Have a Pretty Face",
          date: "January 12, 2019"
        },
        {
          img: "-56",
          title: "Ranking the greatest players in basketball",
          date: "January 12, 2019"
        },
        {
          img: "-57",
          title: "4 Ways to Look Cool in Glasees",
          date: "January 12, 2019"
        },
        {
          img: "-58",
          title: "Top Camper Trailer Towing Tips",
          date: "January 12, 2019"
        },
        {
          img: "-59",
          title: "5 Lovely Walks in New York",
          date: "January 12, 2019"
        },
      ],
      recentPost: [
        {
          img: "-65",
          title: "Main Reaseons To Stop Texting And Driving",
          date: "January 12, 2019"
        },
        {
          img: "-66 (1)",
          title: "Tips to Help You Quickly Prepare your Lunch",
          date: "January 12, 2019"
        },
        {
          img: "-67",
          title: "Why should I buy a smartwatch?",
          date: "January 12, 2019"
        },
        {
          img: "-68",
          title: "The best augmented reality smartglasses",
          date: "January 12, 2019"
        },
        {
          img: "-69",
          title: "12 Healthiest Foods to Eat for Breakfast",
          date: "January 12, 2019"
        },
      ],
      btnRowBlue: ["gadgets", "photography", "lifestyle", "fashion", "recipes", "travel"],
      homePosts: [
        {
          img: '-54',
          day: '12',
          month: 'jan',
          title: 'How to Make Friends as a Grown-Up',
          content: 'Lorem ipsum dolor sit, amet consectetur adipisicing elit. Labore a nostrum, natus, architecto iusto magni officiis dicta magnam quo expedita minima ea fuga reprehenderit molestiae distinctio ex ipsum voluptatem consectetur.',
          author: 'Jhon Doe',
          type: 'Lifestyle, Travel',
          comments: 12,
        },
        {
          img: '-55 (1)',
          day: '17',
          month: 'apr',
          title: 'Simple Ways to Have a Pretty Face',
          content: 'Lorem ipsum dolor sit, amet consectetur adipisicing elit. Labore a nostrum, natus, architecto iusto magni officiis dicta magnam quo expedita minima ea fuga reprehenderit molestiae distinctio ex ipsum voluptatem consectetur.',
          author: 'Jhon Doe',
          type: 'Lifestyle, Travel',
          comments: 20,
        },
        {
          img: '-56 (1)',
          day: '24',
          month: 'feb',
          title: 'Ranking the greatest players in basketball',
          content: 'Lorem ipsum dolor sit, amet consectetur adipisicing elit. Labore a nostrum, natus, architecto iusto magni officiis dicta magnam quo expedita minima ea fuga reprehenderit molestiae distinctio ex ipsum voluptatem consectetur.',
          author: 'Jhon Doe',
          type: 'Lifestyle, Travel',
          comments: 17,
        },
        {
          img: '-58 (1)',
          day: '12',
          month: 'jan',
          title: 'Top Camper Trailer Towing Tips',
          content: 'Lorem ipsum dolor sit, amet consectetur adipisicing elit. Labore a nostrum, natus, architecto iusto magni officiis dicta magnam quo expedita minima ea fuga reprehenderit molestiae distinctio ex ipsum voluptatem consectetur.',
          author: 'Jhon Doe',
          type: 'Lifestyle, Travel',
          comments: 15,
        },
      ],
    }
  }
}
</script>

<style lang="scss">
@import "./style/common.scss";
</style>
