<script>
export default {
    data() {
        return {
        
        };
    }
};
</script>

<template>
    <section class="bg-color">
        <div class="element-image-circle">
            <div class="translate">
                <div class="elementor-image">
                    <img  class="" src="../assets/images/maxcoach-shape-02.png" alt="">
                </div>
            </div>
        </div>
        <div class="element-image-dots">
            <div class="translate">
                <div class="elementor-image">
                    <img  class="" src="../assets/images/maxcoach-shape-09.png" alt="">
                </div>
            </div>
        </div>
        <div class="element-circle">
            <div class="translate">
                <div class="elementor-shape">
                    <div class="shape"></div>
                </div>
            </div>
        </div>
        <div class="container my-container">
            <div class="row">
                <div class="col-12 center my-padding">
                    <h2>
                        Subscribe <span class="green-color weight">Newsletters</span>
                    </h2>
                    <div class="width-p">
                        <p>
                            Enter your email address to register to our newsletter subscription
                            delivered on a regular basis!
                        </p>
                    </div>
                    <div class="input-button d-flex">
                        <div class="input-element">
                            <input class="input-item" type="email" placeholder="Enter your email ">
                        </div>
                        <div class="button">
                            <button>
                                <span>Subscribe</span>
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;

.bg-color {
    position: relative;
}

.input-element {
    width: 80%;
    

}

.element-circle {
    position: absolute;
    left: 283px;
    top: 122px;

    .shape {
        height: 56px;
        width: 56px;
    color: #8FD6CA;
    border-radius: 50%;
    border: 7px solid #8FD6CA;
    }
}

.element-image-dots {
    position: absolute;
    left: 1349px;
    top: 122px;
}

.element-image-circle {
    position: absolute;
    left: 1424px;
    top: 138px;
    z-index: 1;

    .translate {
        --translateX: -16.71875px;
        --translateY: -38.33063209076175px;
        transform: translateX(var(--translateX))translateY(var(--translateY));
        transition: background .3s,border .3s,border-radius .3s,box-shadow .3s,-webkit-box-shadow .3s;
    }
}

.input-item {
    min-height: 52px;
    padding: 3px 20px;
    border-width: 1px 0px 1px 1px;
    border-radius: 5px 0px 0px 5px;
    color: #7e7e7e;
    border-color: #f5f5f5;
    background-color: #f5f5f5;
    font-size: 15px;
    font-weight: 400;
    letter-spacing: 0em;
    border: 1px solid #f5f5f5;
    width: 100%;
}

button {
    @include button-style;
    min-height: 52px;
    padding: 5px 30px;
    border-radius: 0px 5px 5px 0px;

    &:hover {
        background-color: #3f3a64;
        transition: all 0.25s cubic-bezier(0.645, 0.045, 0.355, 1);
    }

    span {
        font-weight: 400;
    }
}

.input-button {
    margin: 0 auto;
    width: 48%;
}

h2 {
    font-weight: 600;
    color: #3f3a64;
    // font-size: 35px;

    .green-color {
        color: #20ad96;
    }

    .weight {
        font-weight: 400;
    }
}

label {
    position: absolute;
    left: 10px;
    font-weight: 200;
    top: 20px;
    color: #9e9e9e;
}

section.bg-color {
    background-color: white;
}

.my-padding {
    padding: 90px 0px 100px 0px;
}

div.center {
    text-align: center;

    div.width-p {
        width: 45%;
        margin: 0 auto;
        margin-top: 18px;
        margin-bottom: 44px;

        p {
            color: #696969;
            font-weight: 400;
            font-size: 18px;
            
        }
    }
        
    
    
}

</style>