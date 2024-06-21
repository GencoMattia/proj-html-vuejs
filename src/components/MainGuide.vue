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
                            <div class="round-points bg-img"></div>
                            <div class="round bg-img"></div>
                            <div class="my_slick">
                                <svg xmlns="http://www.w3.org/2000/svg" version="1.1" width="200px" height="202px" viewBox="0 0 200 202">
                                    <path fill="#e5c791" class="elementor-shape-fill" d="M139.374493,198.087515 C155.702187,206.99353 190.724846,197.001323 197.677982,159.049528 C204.827153,120.027728 184.496324,118.997566 188.045232,104.801934 C202.287755,83.6528313 204.827153,56.662651 190.073179,40.4146034 C153.570125,2.39058926 144.444362,48.0194062 114.025151,20.1351292 C101.727304,7.83728238 83.0989526,-6.73517414 56.2286492,3.40456297 C18.2385839,17.7404371 27.3303985,47.659333 27.3303985,69.3128542 C27.3303985,76.9370868 3.11408002,91.2696589 0.460095291,110.885776 C-2.88628833,135.619549 12.6277797,168.175291 27.3303985,179.329002 C50.6517938,205.692318 86.6478605,199.608476 102.87144,190.482713 C116.802125,182.646702 128.220783,192.003673 139.374493,198.087515 Z"></path>
                                </svg>
                            </div>
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
                            <a href="#" class="my_cl-green fw-bold text-decoration-underline">Download free guidebook &rarr;</a> 
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
    .round-points{
        content: url('../assets/img/maxcoach-shape-05-150x150.png');
        top: 90px;
        left: -75px;
    }
    .round{
        width: 72px;
        height: 72px;
        border-radius: 50%;
        border: 11px solid #ecc5ab;
        top: -40px;
        right: -100px;
    }
    svg{
        position: absolute;
        top: -90px;
        left: -70px;
        z-index: 0;
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