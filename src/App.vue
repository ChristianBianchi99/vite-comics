<script>
import Header from './components/AppHeader.vue';
import Main from './components/AppMain.vue';
import Footer from './components/AppFooter.vue';
export default {
  components:{
    Header,
    Main,
    Footer
  }
}
</script>
<template lang="">
  <div>
    <Header class="try" />
    <Main />
    <Footer />
  </div>
</template>
<style lang="scss" scoped>
  @use './style/generals.scss' as *;
</style>