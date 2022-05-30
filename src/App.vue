<template>
  <div id="app">
    <AppHeader :ElementTop="this.headerTopArray"/>
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
      headerBottomArray: ['home', 'elements', 'features', 'pages', 'portfolio', 'blog', 'shop']
    }
  }
}
</script>

<style lang="scss">
@import "./style/common.scss";
</style>
