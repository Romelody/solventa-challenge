<template>
  <div id="Hero">
    <div :class="{'background': !mobileView}" >
      <div :class="{'mobile-container': mobileView, 'container': !mobileView}">
        <div :class="{'column50': !mobileView, 'intro': !mobileView, 'mobile-intro': mobileView }">
          <h1>Préstamos personales online</h1>
          <p>Una vez iniciado el proceso nuestros asesores especializados se pondrán en contacto para dar por finalizada la solicitud y para que tengas el dinero en tu cuenta, en 5 minutos. Nos destacamos por nuestra velocidad y facilidad para otorgar préstamos en el acto.</p>
        </div>
        <div :class="{'cta-mobile': mobileView, 'mobile-background': mobileView, 'cta': !mobileView, 'column50': !mobileView}">
          <Form/>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Form from './Form.vue'

export default {
  name: 'Hero',
  components: {
    Form
  },
  props: {
    mobileView: Boolean
  }
}
</script>

<style>
  .mobile-container{
    display: flex;
    flex-direction: column;
    width: 85%;
    margin: 0 auto;
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
  .mobile-background{
    background-image: url(../assets/ethnic-young-woman-using-laptop-while-having-tasty-beverage-3768894.jpg);
    background-size: 900px;
    background-position: center; 
  }
  .background{
    background-image: url(../assets/ethnic-young-woman-using-laptop-while-having-tasty-beverage-3768894.jpg);
    background-size: cover;
    background-position: center;
  }

  .column50{
    width: 50%;
  }

  .mobile-intro{
    display: flex;
    flex-direction: column;
    height: 100%;
  }

  .mobile-intro h1{
    display: flex;
    align-items: flex-start;
    justify-content: center;
    height: 100%;
    padding: 40px 0;
    font-size: 25px;
    color: #7f54b3;
  }

  .mobile-intro p{
    display: flex;
    align-items: flex-end;
    height: 100%;
    width: 100%;
    padding-bottom: 50px;
    text-align: center;
    line-height : 30px;
    font-size: 14px;
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

  .cta-mobile{
    display: flex;
    justify-content: center;
    height: 100%;
    align-items: flex-end;
    padding: 50px 0;
  }

  .cta-mobile p{
    font-size: 13px;
    display: flex;
    padding: 10px;
  }

  .cta{
    display: flex;
    justify-content: flex-end;
    height: 100%;
    align-items: flex-end;
    padding-bottom: 50px;
  }
</style>
