<template>
    <div id="form">
        <p class="ctaBtn" @click="showModal=true">Solicitar Préstamo ahora!</p>
        <transition name="fade" appear>
            <div class="modalOverlay" v-show="showModal || showSecondModal">
                <div class="modals">
                    <div v-if="showModal">
                        <form class="modal" @submit.prevent="onSubmit">
                            <div>
                                <label for="name">Nombre</label>
                                <input id="name" v-model="name" required>
                            </div>
                            <div>
                                <label for="phone">Telefono</label>
                                <input id="phone" v-model.number="phone" required>
                            </div>
                            <div>
                                <label for="dni">Dni</label>
                                <input id="dni" v-model.number="dni" required>
                            </div>
                            <p class="sendBtn">
                                <input type="submit" class="send" @click=" showSecondModal=true; bounce=!bounce; showModal=false;" value="Send">
                            </p>
                        </form>
                    </div>
                <transition name="bounce" >
                    <div class="thanks" v-show="bounce" @click=" showSecondModal=false; bounce=!bounce;" >
                        <p>Gracias por completar el formulario</p>
                    </div>
                </transition>
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
            phone:null,
            dni:null,
            showModal:false,
            showSecondModal:false,
            bounce:false,
        }
    }
}
</script>

<style>

.ctaBtn, .send{
    font-family: Montserrat,sans-serif;
    height: 60px;
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

.sendBtn{
    display: flex;
    justify-content: center;
}

.send{
    padding: 0 60px;
}

.ctaBtn{
    background: #7f54b3;
    color: #fff;
}

p.ctaBtn:hover{
    box-shadow: 6px 6px rgba(0, 0, 0, 0.6);
    background: #fff;
    border: solid 2px #7f54b3;
    color: #7f54b3;
}

.sendBtn input:hover{
    box-shadow: 6px 6px rgba(0, 0, 0, 0.6);
}

.modalOverlay{
    position: fixed ;
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
    width: 100%;
    max-height: 500px;
    max-width: 600px;
    background: #fff;
    border-radius: 5px;
    padding: 30px;
}

.modals{
    display: flex;
    width: 100%;
    height: 100%;
    justify-content: center;
    align-items: center;

}

.thanks{
    padding: 50px;
}

.modal div{
    padding: 20px;
    text-align: left;
}

.modal  input{
    border:0px;
    border-bottom: 1px solid rgba(0, 0, 0, 0.1);
    width: 100%;
    }

.thanks p{
    font-size: 20px;
    text-align: center;
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%,-50%);
    line-height : 30px;
    white-space: nowrap;
}

.bounce-enter-active{
    animation: bounce-in .5s forwards;
}
.bounce-leave-active{
    animation: bounce-in .5s reverse;
}

@keyframes bounce-in{

    0%{
        transform:scale(0);
    }
    50%{
        transform: scale(1.5);
    }
    100%{
        transform: scale(1);
    }
}

</style>