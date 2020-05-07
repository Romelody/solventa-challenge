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
    topNav , hero, footerMenu, slider
  }
}
</script>

<style>
  @import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@600&family=Roboto&display=swap");

#app {
  font-family: Roboto, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  background: #F7F7F7;
}

*{
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

li, a, button{
  color: black;
  text-decoration: none;
}

p{
  text-align: left;
}
.container{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    flex-wrap: wrap;
    align-items: center;
    padding: 30px 0;
    margin: 0 auto;
    width: 85%;
    height: 500px;
}
</style>
