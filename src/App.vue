<template>
  <div id="app">
    <AppHeader :ElementTop="this.headerTopArray" :ElementBottom="this.headerBottomArray"/>
    <AppMain />
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
      ]
    }
  }
}
</script>

<style lang="scss">
@import "./style/common.scss";
</style>
