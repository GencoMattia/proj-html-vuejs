<script>
import { FontAwesomeIcon } from '../js/font-awesome.js';
export default {
    components:{
        FontAwesomeIcon
    },
    data() {
        return {
            
    }}
}
</script>

<template>
    <div class="my-container">
        <div class="container">
            <section class="row">
                <div class="col-6 position-relative">
                        <img src="../assets/img/home-2-popup-video-poster.jpg" alt="">
                    <div class="my_bg-move">
                        <div class="top-image"></div>
                    </div>
                </div>
                <article class="col-6">
                    <p class="my_cl-blue">
                        GET STARTED <span class="fw-bold">EFFORTLESSLY</span>
                    </p>
                    <h2>
                        <span class="my_cl-blue fw-bold">Enjoy Our</span> <br>
                        <span class="my_cl-green">Companionship</span>
                    </h2>
                    <p>
                        Sneek peek into what has in store for you on our online teaching and mentoring portal. Seek for some hidden hints of early-bird rewards as well.
                    </p>
                    <p>
                        <a href="#" class="my_cl-green fw-bold">Download free guidebook <font-awesome-icon :icon="['fas', 'arrow-right']"/></a> 
                    </p>
                </article>
                
            </section>
        </div>
    </div>
</template>

<style scoped>
    img{
        width: 100%;
        border-radius: 5px;
    }
    .top-image {
    content: url('../assets/img/icon-youtube-play.png');
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    background-size: contain;
    background-repeat: no-repeat;
    width: 15%;
    }
    .my_cl-green{
        color: #20ad96;
    }
    .my_cl-blue{
        color: #3f3a64;
    }
</style>