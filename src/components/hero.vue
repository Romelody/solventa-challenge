<template>
    <div id="hero">
        <div class="background">
            <div class="container">
                <div class="column50 intro">
                    <h1>Dale careta, necesitas plata</h1>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolores sequi debitis iste, nisi maxime tempora praesentium itaque suscipit accusamus magnam numquam ad? Aperiam a deleniti eveniet harum repellendus ullam soluta.</p>
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
.column50{
    width: 50%;
}

.intro h1{
    display: flex;
    justify-items: ;
}

.cta{
    display: flex;
    justify-content: flex-end;
}

h1{
    font-size: 45px;
    text-align: left;
}

p{
    text-align: left;
}

</style>