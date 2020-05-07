<template>
  <div id="topNav">
    <header>
      <img :src="logo" class="logo"/>
      <div id="navIcon" v-if="mobileview">
        <i class="fas fa-bars"></i>
      </div>
      <nav v-if="!mobileView">
        <ul class="nav-links">
          <li><a href="#">Sucursal</a></li>
          <li><a href="#">¿Que necesito?</a></li>
          <li><a href="#">Ayuda</a></li>
        </ul>
      </nav>
    </header>
  </div>
</template>

<script>
  import logo from "../assets/logo.png"

  export default {
    data(){
      return{
        logo:logo,
        mobileView:true,
        showNav:false
      }
    }
  }
</script>

<style>
#navIcon{
  padding: 10px;
  margin: 10px;
  cursor: pointer;
}
  i{
    font-size: 2rem;
  }

#topNav{
  background-color: #fff;
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
</style>
