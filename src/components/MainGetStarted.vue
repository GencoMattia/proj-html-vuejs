<script>
export default {
    data() {
        return {
        
        };
    }
};
</script>

<template>
    <section class="my-container get-started text-center">
        <div class="elements-wrapper">
            <h2>
                Start today for getting <span>Online Certification</span>
            </h2>
    
            <h1>
                You can be your own guiding star with our help!
            </h1>
            <button class="get-started-button">
                Get started now
            </button>
        </div>
        <div class="background-landscape">
            <img class="stripes-shape" src="../assets/img/maxcoach-shape-01.png" alt="maxcoach-shape-01">
            <img class="semicircles-shape" src="../assets/img/maxcoach-shape-02.png" alt="maxcoach-shape-02">
            <div class="circle-shape">

            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
@use "../styles/partials/mixins" as *;

section {
    position: relative;
    color: #3f3a64;
    padding: 3rem 0;

    .elements-wrapper {
        position: relative;
        z-index: 2;

        h2 {
            font-size: 1.5rem;
            font-weight: 700;
    
            span {
                font-weight: 600;
                color: #20AD96;
            }
        }
    
        h1 {
            font-size: 2rem;
            font-weight: 700;
            margin-bottom: 2.5rem
        }
        
        button {
            @include button-style;
            padding: .9rem 4.5rem;
        }
    }
    
    .background-landscape {
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
        z-index: 1;

        .stripes-shape {
            position: absolute;
            left: 10px;
            bottom: 20px;
        }

        .semicircles-shape {
            position: absolute;
            right: 10px;
            top: 20px;
        }
    }
}


</style>