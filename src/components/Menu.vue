<template>
  <div>
    <div class="navIcon" v-if="mobileView && !clicked" @click="clicked = !clicked">
      <i class="fas fa-bars"></i>
    </div>
    <nav v-if="!mobileView || (mobileView && clicked)">
      <ul :class="{'mobile-nav-links': mobileView, 'nav-links': !mobileView}" v-if="clicked || !mobileView">
        <li><a href="#">Sucursal</a></li>
        <li><a href="#">¿Que necesito?</a></li>
        <li><a href="#">Ayuda</a></li>
      </ul>
      <div @click="clicked = !clicked" class="close" v-if="mobileView">X</div>
    </nav>
  </div>
</template>

<script>
  export default {
    name:'Menu',
    data(){
      return{
        clicked: false
      }
    },
    props: {
      mobileView: Boolean
    }
  }
</script>

<style>
  i{
    font-size: 2rem;
  }
  .navIcon{
    padding: 15px;
    width: 50px;
  }
  .mobile-nav-links{
    list-style: none;
    display: flex;
    flex-direction: column;
    padding: 8px 4px;
  }

  .mobile-nav-links li {
    display: inline-block;
    padding: 8px;
  }

  .mobile-nav-links li a {
    transition: all 0.3s ease 0s;
    margin: 8px 4px 8px 4px;
  }

  .mobile-nav-links li a:hover{
    color: #7f54b3;
  }

  .nav-links{
    list-style: none;
  }

  .nav-links li {
    display: inline-block;
    padding: 0px 20px;
  }

  .nav-links li a {
    transition: all 0.3s ease 0s;
  }

  .nav-links li a:hover{
    color: #7f54b3;
  }

  .close{
    position:fixed;
    top:0;
    right: 0;
  }
</style>