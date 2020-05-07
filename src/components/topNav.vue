<template>
  <div id="topNav">
    <header>
      <img :src="logo" class="logo"/>
      <Menu :mobileView="mobileView"/>
    </header>
  </div>
</template>

<script>
  import logo from "../assets/logo.png"
  import Menu from './Menu'

  export default {
    name:'topNav',
    data(){
      return{
        logo:logo
      }
    },
    props: {
      mobileView: Boolean
    },
    components:{
      Menu
    }
  }
</script>

<style>

  #topNav{
    background-color: white;
  }

  header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 85%;
    padding: 30px 0;
    margin: 0 auto;
  }

  .logo{
    cursor:pointer;
    width: 200px;
  }
</style>
