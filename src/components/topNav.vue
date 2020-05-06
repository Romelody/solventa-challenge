<template>
  <div id="topNav">
    <header>
      <img :src="logo" class="logo"/>
      <nav>
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
      }
    }
  }
</script>

<style>
*{
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

li, a, button{
    color: black;
    text-decoration: none;
}

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
