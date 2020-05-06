<template>
  <div id="app">
    <topNav/>
    <hero/>
    <slider/>
    <footerMenu/>
  </div>
</template>

<script>
import topNav from './components/topNav.vue'
import hero from './components/hero.vue'
import slider from './components/slider.vue';
import footerMenu from './components/footerMenu.vue'

export default {
  name: 'App',
  components: {
    topNav , hero, slider, footerMenu,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 40px;
  background: #F7F7F7;
}
</style>
