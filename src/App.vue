<template>
  <div id="app">
    <topNav :mobileView="mobileView"/>
    <Hero :mobileView="mobileView"/>
    <Slider :mobileView="mobileView"/>
    <Footer/>
  </div>
</template>

<script>

import topNav from './components/topNav.vue'
import Hero from './components/Hero.vue'
import Slider from './components/Slider.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    topNav , Hero, Footer, Slider
  },
  data(){
    return{
      mobileView:true,
      showNav:false,
    }
  },
  methods:{
    handleView(){
      this.mobileView = window.innerWidth <= 900;
    }
  },
  created(){
    this.handleView();
    window.addEventListener('resize',this.handleView)
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
</style>
