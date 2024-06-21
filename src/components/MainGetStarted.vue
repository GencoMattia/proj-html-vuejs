<script>
export default {
    data() {
        return {
        
        };
    }
};
</script>

<template>
    <article class="bg-color">
        <section class="my-container get-started text-center">
            <div class="elements-wrapper">
                <h4>
                    Start today for getting <span>Online Certification</span>
                </h4>
        
                <h2>
                    You can be your own guiding star with our help!
                </h2>
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
    </article>
</template>

<style scoped lang="scss">
@use "../styles/partials/mixins" as *;

.bg-color {
    background-color: #f8f8f8;
    padding-top: 3rem;
    padding-bottom: 3rem;
}

section {
    position: relative;
    color: #3f3a64;
    padding: 3rem 0;

    .elements-wrapper {
        position: relative;
        z-index: 2;

        h4 {
            // font-size: 1.5rem;
            font-weight: 600;
    
            span {
                font-weight: 400;
                color: #20AD96;
            }
        }
    
        h2 {
            // font-size: 2rem;
            font-weight: 600;
            margin-bottom: 2.5rem
        }
        
        button {
            @include button-style;
            padding: .9rem 4.5rem;

            transition: all .3s ease;

            &:hover {
                background-color: #3f3a64;
            }
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

        .circle-shape {
            position: absolute;
            left: 40px;
            width: 52px;
            height: 52px;
            border-radius: 50%;
            border: 7px solid #E6DCD2;
        }
    }
}


</style>