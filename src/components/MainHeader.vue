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
                <article class="col-5 d-flex flex-column justify-content-center pe-5 my_cl-blue">
                    <h1>
                        Distant learning for further expansion
                    </h1>
                    <p>
                        Learning is a life-long journey that in fact we never find the terminate stop. Stop searching, enjoy the process.
                    </p>
                    <div>
                        <button class="button-style my-4">
                            <font-awesome-icon icon="fa-solid fa-download" /> Download free guide
                        </button>
                    </div>
                    <p>
                        Have questions? <a href="#" class="my_cl-green fw-bold text-decoration-underline">Get Free Sample <font-awesome-icon :icon="['fas', 'arrow-right']"/></a>
                    </p>
                </article>
                <div class="col-7 d-flex justify-content-center position-relative p-0">
                    <div>
                        <img src="../assets/img/about-me-profile-ohm4dxoearqbxny7q3bq1pzbdgofdx0tobbeqcvzd0.jpg" alt="about-me-profile">
                        <div class="charge bg-img"></div>
                        <div class="square bg-img"></div>
                        <div class="round bg-img"></div>
                        <div class="square-transparent-up bg-img"></div>
                        <div class="square-transparent-down bg-img"></div>
                    </div>
                </div>
            </section>
        </div>
    </div>
</template>

<style scoped lang="scss">
    @use '../styles/partials/mixins' as *; 

    section{
        padding: 4rem 0;
    }

    h1{
        font-weight: 700;
    }

    img{
        border-radius: 50%;
        position: relative;
        z-index: 2;
    }
    .my_bg-move {
    padding: 25px;
    width: 35%;
    height: 35%;
    position: absolute;
    top: 100px;
    }
    .bg-img{
        position: absolute;
        z-index: 1;
    }
    .square{
        content: url('../assets/img/maxcoach-shape-07-150x150.png');
        right: 152px;
        bottom: 5px;
    }
    .square-transparent-up{
        content: url('../assets/img/maxcoach-shape-08.png');
        top: 170px;
        left: -25px;
    }
    .square-transparent-down{
        content: url('../assets/img/maxcoach-shape-08.png');
        bottom: 125px;
        left: -25px;
    }
    .charge{
        content: url('../assets/img/maxcoach-shape-02.png');
        top: 120px;
        right: -50px;
        z-index: 3;
    }
    .round{
        width: 62px;
        height: 62px;
        border-radius: 50%;
        border: 8px solid #ecc5ab;
        bottom: 125px;
        left: 32px;
        z-index: 3;
    }
    button{
        @include button-style();
        padding: 1rem 2.5rem;

        transition: all .3s ease;

        &:hover {
            background-color: #3f3a64;
        }
    }
    .my_cl-green{
        color: #20ad96;
    }
    .my_cl-blue{
        color: #3f3a64;
    }
</style>