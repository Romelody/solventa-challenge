<template>
  <div id="slider" class="containerSlider">
    <div class="containerSlide">
      <h2>Beneficios Exclusivos</h2>
      <carousel :perPageCustom="[[0, 1], [480, 1], [768, 1]]">
        <slide :class="{'sliderImg-mobile': mobileView, 'sliderImg': !mobileView } " v-for="(image, index) in images" :key="index">
          <img :src="image" >
        </slide>
      </carousel>
    </div>
  </div>
</template>

<script>
  import { Carousel, Slide } from 'vue-carousel';
  import slider01 from "../assets/slider01.jpg"
  import slider02 from "../assets/slider02.jpg"

  export default {
    name: "Slider",
    components: {
      Carousel, Slide
    },
    data(){
      return{
        images:[
          slider01,
          slider02
        ],
        imageActiv:slider01,
        show: 0
      }
    },
    props: {
      mobileView: Boolean
    },
    methods:{
      slides:function(index) {
        this.imageActiv = this.images[index];
      }
    }
  }
</script>

<style>
  .containerSlider{
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    align-items: center;
    padding: 30px 0;
    margin: 0 auto;
  }

  .containerSlide{
    width: 100%;
    height: 100%;
    margin: 0 auto;
    margin-bottom: 3rem;
    background: #ffffff;
    box-shadow: 0px 3px 12px -1px rgba(0,0,0,0.42);
  }

  .containerSlide h2{
    font-family: Montserrat,sans-serif;
    padding: 30px;
    color: #858585;
  }

  .sliderImg-mobile{
    height: 150px;
  }

  .sliderImg-mobile img{
    height: 150px;
    border-radius: 30px;
  }

  .sliderImg img{
    height: 300px;
    border-radius: 30px;
  }

  .sliderImg {
    height: 300px;
  }

  .sliderMenu{
    width: 100%;
    margin: 0 auto;
    margin-top: 20px;
  }

  .sliderMenu a{
    margin: 15px;
    color: #858585;
  }
</style>
