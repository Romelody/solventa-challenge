<template>
    <div id="form">
        <p class="cta" @click="showModal=true">Solicitar Préstamo ahora!</p>

        <transition name="fade" appear>
            <div class="modalOverlay" v-show="showModal || showSecondModal">
                <div v-if="showModal">
                    <form class="modal" @submit.prevent="onSubmit">
                        <p>
                            <label for="name">Name</label>
                            <input id="name" v-model="name" required>
                        </p>
                        <p>
                            <label for="telefono">Phone</label>
                            <input id="telefono" v-model.number="telefono" required>
                        </p>
                        <p>
                            <label for="dni">Dni</label>
                            <input id="dni" v-model.number="dni" required>
                        </p>
                        <p>
                            <input type="submit" class="send" @click="showSecondModal=true; showModal=false;" value="Send">
                        </p>
                    </form>
                </div>
                <div v-if="showSecondModal">
                    <div class="thanks" @click="showSecondModal=false;">
                        <p>Gracias por completar el formulario</p>
                    </div>
                </div>
            </div>
        </transition>
        
    </div>
</template>
<script>
export default {
    data(){
        return{
            name:null,
            telefono:null,
            dni:null,
            showModal:false,
            showSecondModal:false,
        }
    }
}
</script>
<style>

p.cta, .send{
    appearance: none;
    cursor: pointer;
    background: #7f54b3;
    padding: 20px;
    border-radius: 5px;
    text-transform: uppercase;
    text-align: center;
    color: #fff;
    box-shadow: 3px 3px rgba(0,0,0,0.4);
    transition: 0.4s ease-out;
    align-items: center;
    
}

p.cta:hover{
    box-shadow: 6px 6px rgba(0, 0, 0, 0.6);
}

.modalOverlay{
    position: absolute ;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    z-index: 98;
    background-color: rgba(0, 0, 0, 0.4);
}

.fade-enter-active, fade-leave-active {
    transition: opacity 1s;
}
.fade-enter,fade-leace-to{
    opacity: 0;
}
.fade-leave-to{
    opacity: 0;
}

.modal, .thanks{
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%,-50%);
    z-index: 99;

    width: 100%;
    height: 300px;
    max-width: 600px;
    background: #fff;
    border-radius: 5px;
    padding: 30px;
}
.modal p{
    padding: 20px;
}

.modal p input{
    border:0px;
    border-bottom: 1px;
}

.thanks p{
    font-size: 20px;
    text-align: center;
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%,-50%);
    line-height : 30px;
}

</style>