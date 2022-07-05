<template>
  <div id="app">
  <div class="container">
    <HeaderNav/>
    <router-view/>
    <HeroSection/>
  </div>
  </div>
</template>

<script>
import HeaderNav from './components/HeaderNav.vue';
import HeroSection from './components/HeroSection.vue';
export default {
  name: "App",
  components: {
    HeaderNav,
    HeroSection,
   
  }
};
</script>
<style lang="scss">
@import './reset.css';



nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
