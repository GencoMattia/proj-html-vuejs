<script>
import { FontAwesomeIcon } from '../js/font-awesome';

export default {
    components: {
        FontAwesomeIcon,
    },

    data() {
        return {
            clientsCards: [
                {
                    icon: "client-logo-01.png"
                },
                {
                    icon: "client-logo-02.png"
                },
                {
                    icon: "client-logo-03.png"
                },
                {
                    icon: "client-logo-04.png"
                },
                {
                    icon: "client-logo-05.png"
                },
                {
                    icon: "client-logo-06.png"
                },
                {
                    icon: "client-logo-07.png"
                }
            ],

            scrollPosition: 0,
        };
    },

    methods: {
        getImagePath: function(img) {
            return new URL(`../assets/img/${img}`, import.meta.url).href;
        },

        prevCard() {
            const cardWidth = this.$refs.carouselRow.querySelector('.col-2').offsetWidth;
            this.scrollPosition = Math.max(0, this.scrollPosition - cardWidth);
            this.$refs.carouselRow.scrollTo({ left: this.scrollPosition, behavior: 'smooth' });
        },

        nextCard() {
            const cardWidth = this.$refs.carouselRow.querySelector('.col-2').offsetWidth;
            const maxScroll = this.$refs.carouselRow.scrollWidth - this.$refs.carouselRow.offsetWidth;
            this.scrollPosition = Math.min(maxScroll, this.scrollPosition + cardWidth);
            this.$refs.carouselRow.scrollTo({ left: this.scrollPosition, behavior: 'smooth' });
        },
    },

    computed: {
        
    },

    mounted() {
        this.carouselRow = this.$refs.carouselRow;
    },

};
</script>

<template>
    <div class="my-container row mb-5">
        <div class="carousel-prev-button col-1">
            <button class="prev-card" @click="prevCard">
                <font-awesome-icon icon="chevron-left" />
            </button>
        </div>
        <div class="carousel-container col-10">
            <div class="carousel-row row" ref="carouselRow">
                <article class="col-2" v-for="(logo, index) in clientsCards" :key="index">
                    <img :src="getImagePath(logo.icon)" alt="client-logo">
                </article>
            </div>
        </div>
        <div class="carousel-next-button col-1">
            <button class="next-card" @click="nextCard">
                <font-awesome-icon icon="chevron-right" />
            </button>
        </div>
    </div>
</template>

<style scoped lang="scss">
@use "../styles/partials/mixins" as *;

.carousel-row {
    display: flex;
    flex-wrap: nowrap;
    overflow-x: hidden;
    scroll-snap-type: x mandatory;

    &::-webkit-scrollbar {
        display: none;
    }

    article {
        display: flex;
        justify-content: center;
        align-items: center;
        scroll-snap-align: center;

        img {
            opacity: .5;
            transition: opacity .3s ease;
        }

        &:hover {
            img {
                opacity: 1;
            }
        }
    }
}

.carousel-prev-button,
.carousel-next-button {
    display: flex;
    justify-content: center;

    button {
        background-color: transparent;
        border: none;
        color: #8c89a2;
        opacity: .5;

        &:hover {
            opacity: 1;
        }
    }
}
</style>