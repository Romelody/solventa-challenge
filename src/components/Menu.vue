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
    width: 50px;
  }
  .mobile-nav-links{
    position: fixed;
    top:0;
    right:0;
    list-style: none;
    display: flex;
    flex-direction: column;
    padding: 1rem;
    background: white;
    height: 100%;
    margin-top: 30px;
    z-index: 2;
  }

  .mobile-nav-links li {
    display: flex;
    justify-content: flex-end;
    padding: 1rem;
    border-bottom: 1px solid #7f54b3;
  }

  .mobile-nav-links li a {
    transition: all 0.3s ease 0s;
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
    top: 1rem;
    right: 2rem;
    color: #fff;
    background: #7f54b3;
    padding: 2px 5px;
    border-radius: 4px;
    z-index: 3;
  }
</style>