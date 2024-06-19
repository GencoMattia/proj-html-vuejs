<script>
export default {
    data() {
        return {
        movementStrength: 25,
        w: window.innerWidth,
        h: window.innerHeight,
        newvalueX: 0,
        newvalueY: 0
    }},
    methods: {
        handleMouseMove(e) {
            const pageX = (e.pageX - this.w / 2) / this.w / 2;
            const pageY = (e.pageY - this.h / 2) / this.h / 2;
            this.newvalueX = pageX * this.movementStrength;
            this.newvalueY = pageY * this.movementStrength;
        }
    },
    mounted() {
        window.addEventListener('mousemove', this.handleMouseMove);
    },
    beforeDestroy() {
        window.removeEventListener('mousemove', this.handleMouseMove);
    }
}
</script>

<template>
    <div class="my-container">
        <div class="container">
            <section class="row">
                <article class="col-6">
                    <h2>
                        Distant learning for further expansion
                    </h2>
                    <p>
                        Learning is a life-long journey that in fact we never find the terminate stop. Stop searching, enjoy the process.
                    </p>
                    <button>
                        Download free guide
                    </button>
                    <p>
                        Have questions? <a href="#">Get Free Sample</a>
                    </p>
                </article>
                <div class="col-6 ciao">
                        <img src="../assets/img/about-me-profile-ohm4dxoearqbxny7q3bq1pzbdgofdx0tobbeqcvzd0.jpg" alt="">
                    <div class="my_bg-move">
                        <div ref="topImage" class="top-image" :style="{ left: newvalueX + 'px', top: newvalueY + 'px' }"></div>
                    </div>
                </div>
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
    .ciao{
        position: relative;
    }
</style>