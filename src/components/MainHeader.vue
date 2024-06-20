<script>
export default {
    data() {
        return {

    }}
}
</script>

<template>
    <div class="my-container">
        <div class="container">
            <section class="row">
                <div class="col-6 ciao">
                        <img src="../assets/img/about-me-profile-ohm4dxoearqbxny7q3bq1pzbdgofdx0tobbeqcvzd0.jpg" alt="">
                    <div class="my_bg-move">
                        <div class="top-image"></div>
                    </div>``
                </div>
                <article class="col-6">
                    <h2>
                        Distant learning for further expansion
                    </h2>
                    <p>
                        Learning is a life-long journey that in fact we never find the terminate stop. Stop searching, enjoy the process.
                    </p>
                    <button>
                        <font-awesome-icon icon="fa-solid fa-download" /> Download free guide
                    </button>
                    <p>
                        Have questions? <a href="#">Get Free Sample</a>
                    </p>
                </article>
                
            </section>
        </div>
    </div>
</template>

<style scoped>
    img{
        border-radius: 50%;
    }
    .my_bg-move {
    padding: 25px;
    width: 35%;
    height: 35%;
    position: absolute;
    top: 100px;
    }

    .top-image {
    background: url('../assets/img/maxcoach-shape-02.png');
    position: absolute;
    background-size: contain;
    width: 25%;
    z-index: 0;
    height: 100%;
    background-repeat: no-repeat;
    }
</style>