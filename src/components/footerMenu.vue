<template>
    <div id="footerNav">
        <footer>
            <ul class="footer-links">
            <li><a href="#">Sucursal</a></li>
            <li><a href="#">¿Que necesito?</a></li>
            <li><a href="#">Ayuda</a></li>
            </ul>
        </footer>
    </div>
</template>

<script>
export default {
    
}
</script>

<style>
#footerNav{
    background: #515365;
}

footer li a{
    color: #fff;
    text-decoration: none;
}

footer {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 85%;
    padding: 30px 0;
    margin: 0 auto;
}
.footer-links{
  list-style: none;
}

.footer-links li {
  display: inline-block;
  padding: 0px 20px;
}

.footer-links li a {
  transition: all 0.3s ease 0s;
}

.footer-links li a:hover{
  color: #858585;
}
</style>