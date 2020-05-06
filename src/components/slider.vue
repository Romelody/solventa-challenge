<template>
    <div id="slider" class="container">
        <div class="containerSlide">
            <div>
                <h2>Beneficios Exclusivos</h2>
            </div>
            <div class="sliderImg">
                <img :src="imageActiv" alt="">
            </div>
            <div class="sliderMenu">
                <a href="" @click.prevent="slides(0)"> ● </a>
                <a href="" @click.prevent="slides(1)"> ● </a>
            </div>
        </div>

    </div>
</template>

<script>
import slider01 from "../assets/slider01.jpg"
import slider02 from "../assets/slider02.jpg"

export default {
    data(){
        return{
            images:[
                slider01,
                slider02
            ],
            imageActiv:slider01
        }
    },
    methods:{
        slides:function(index) {
            this.imageActiv = this.images[index];
    }
    }
}
</script>

<style>
.container{
    
}

.containerSlide{
    width: 100%;
    height: 100%;
    margin: 0 auto;
    border-radius: 30px;
    background: #ffffff;
    -webkit-box-shadow: 0px 3px 12px -1px rgba(0,0,0,0.42);
    -moz-box-shadow: 0px 3px 12px -1px rgba(0,0,0,0.42);
    box-shadow: 0px 3px 12px -1px rgba(0,0,0,0.42);
}

.containerSlide h2{
    padding: 30px;
    color: #858585;
}

.sliderImg img{
    height: 300px;
    border-radius: 30px;
}

.sliderImg {
    width: 100%;
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