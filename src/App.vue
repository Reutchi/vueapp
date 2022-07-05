<template>
  <div id="app">
  <div class="container">
    <HeaderNav/>
    <router-view/>
    <HeroSection/>
  </div>
    <ProjectsSection/>

  </div>
</template>

<script>
import HeaderNav from './components/HeaderNav.vue';
import HeroSection from './components/HeroSection.vue';
import ProjectsSection from './components/ProjectsSection.vue';
export default {
  name: "App",
  components: {
    HeaderNav,
    HeroSection,
    ProjectsSection,
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
