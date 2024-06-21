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

        </div>
    </section>
</template>

<style scoped lang="scss">
@use "../styles/partials/mixins" as *;

section {
    position: relative;
    color: #3f3a64;

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
    
    
    
}


</style>