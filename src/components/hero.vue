<template>
    <div id="hero">
        <div class="background">
            <div class="container">
                <div class="column50 intro">
                    <h1>Préstamos personales online</h1>
                    <p>Una vez iniciado el proceso nuestros asesores especializados se pondrán en contacto para dar por finalizada la solicitud y para que tengas el dinero en tu cuenta, en 5 minutos. Nos destacamos por nuestra velocidad y facilidad para otorgar préstamos en el acto.</p>
                </div>
                <div class="column50 cta">
                    <formulario/>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import formulario from './formulario.vue'

export default {
    name: 'App',
        components: {
        formulario,
  }
}
</script>

<style>
.background{
    background-image: url(../assets/ethnic-young-woman-using-laptop-while-having-tasty-beverage-3768894.jpg);
    background-size: cover;
    background-position: center;
}

.column50{
    width: 50%;
}

.intro{
    display: flex;
    flex-direction: column;
    height: 100%;
}

.intro h1{
    display: flex;
    align-items: flex-start;
    height: 100%;
    padding-top: 150px ;
    font-size: 45px;
    text-align: left;
    color: #7f54b3;
}

.intro p{
    display: flex;
    align-items: flex-end;
    height: 100%;
    width: 80%;
    padding-bottom: 50px;
    text-align: left;
    line-height : 40px;
    
}

.cta{
    display: flex;
    justify-content: flex-end;
    height: 100%;
    align-items: flex-end;
    padding-bottom: 50px;
}
</style>