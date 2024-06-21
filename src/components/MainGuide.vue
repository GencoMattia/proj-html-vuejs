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
    <div class="bg-gray">
    <div class="bg-curve">
        <div class="my-container">
            <div class="container">
                <section class="row">
                    <div class="col-7 position-relative p-0">
                        <div class="my_pos rounded">
                            <img src="../assets/img/home-2-popup-video-poster.jpg" alt="">
                        </div>
                        <div class="my_bg-move">
                            <div class="top-image"></div>
                            <div class="square bg-img"></div>
                            <div class="round bg-img"></div>
                        </div>
                    </div>
                    <article class="col-5 d-flex flex-column justify-content-center">
                        <p class="my_cl-blue">
                            GET STARTED <span class="fw-bold">EFFORTLESSLY</span>
                        </p>
                        <h2 class="fs-1">
                            <span class="my_cl-blue fw-bold">Enjoy Our</span> <br>
                            <span class="my_cl-green">Companionship</span>
                        </h2>
                        <p class="py-5">
                            Sneek peek into what has in store for you on our online teaching and mentoring portal. Seek for some hidden hints of early-bird rewards as well.
                        </p>
                        <p class="py-2">
                            <a href="#" class="my_cl-green fw-bold">Download free guidebook <font-awesome-icon :icon="['fas', 'arrow-right']"/></a> 
                        </p>
                    </article>
                </section>
            </div>
        </div>
    </div>
    </div>
</template>

<style scoped lang="scss">
.bg-gray{
    background-color: #f8f8f8;
}
    .bg-curve{
        border-radius: 0 0 50% 0;
        background-color: white;
    }
    section{
        padding: 7rem 0;
    }
    article{
        padding: 0 4rem;
    }
    img{
        width: 100%;
        transition: transform 0.8s ease;
        position: relative;
        z-index: 2;
    }
    img:hover{
        transform: scale(1.1);
        transition: transform 0.8s ease;
    }
    .top-image {
    content: url('../assets/img/icon-youtube-play.png');
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    background-size: contain;
    background-repeat: no-repeat;
    width: 13%;
    z-index: 3;
    }
    .bg-img{
        position: absolute;
        z-index: 1;
    }
    .square{
        content: url('../assets/img/maxcoach-shape-07-150x150.png');
        right: -15px;
        bottom: -95px;
    }
    .round{
        content: url('../assets/img/maxcoach-shape-05-150x150.png');
        top: 90px;
        left: -75px;
    }
    .my_cl-green{
        color: #20ad96;
    }
    .my_cl-blue{
        color: #3f3a64;
    }
    .my_pos{
        position:relative; 
        overflow:hidden;
    }
</style>