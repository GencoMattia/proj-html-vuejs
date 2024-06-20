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

            currentCardIndex: 0,
            visibleCardCount: 6,
        };
    },

    methods: {
        getImagePath: function(img) {
            return new URL(`../assets/img/${img}`, import.meta.url).href;
        },

        prevCard() {
            const container = this.$refs.carouselContainer;

            if (container.scrollLeft === 0) {
                container.scrollLeft = (this.clonedCards.length - this.visibleCardCount) * container.offsetWidth / this.visibleCardCount; 
            } else {
                container.scrollLeft -= container.offsetWidth;
            }
        },

        nextCard() {
            const container = this.$refs.carouselContainer;

            if (container.scrollLeft >= (this.clonedCards.length - this.visibleCardCount) * container.offsetWidth / this.visibleCardCount) {
                container.scrollLeft = 0;
            } else {
                container.scrollLeft += container.offsetWidth;
            }
        },

        updateVisibleCardCount() {
            const containerWidth = this.$refs.carouselContainer.offsetWidth;
            const cardWidth = this.$refs.carouselContainer.querySelector('.col-2').offsetWidth;
            this.visibleCardCount = Math.floor(containerWidth / cardWidth);
        },
    },

    computed: {
        clonedCards() {
            const firstSix = this.clientsCards.slice(0, 6);
            const lastSix = this.clientsCards.slice(-6);
            return [...lastSix, ...this.clientsCards, ...firstSix];
        },
    },

    mounted() {
        this.updateVisibleCardCount();
    },
};
</script>

<template>
    <div class="my-container row">
        <div class="carosel-prev-button col-1">
            <button class="prev-card" @click="prevCard">
                <font-awesome-icon icon="chevron-left" />
            </button>
        </div>
        <div class="carosel-container col-10" ref="carouselContainer">
            <div class="carosel-row row">
                <article class="col-2"
                v-for="(logo, index) in clonedCards" :key="index">
                    <img :src="getImagePath(logo.icon)" alt="client-logo">
                </article>
            </div>
        </div>
        <div class="carosel-next-button col-1">
            <button class="next-card" @click="nextCard">
                <font-awesome-icon icon="chevron-right" />
            </button>
        </div>
    </div>
</template>

<style scoped lang="scss">
@use "../styles/partials/mixins" as *;

    .carosel-container {
    overflow-x: hidden;
    }

    .carosel-row {
        display: flex;
        flex-wrap: nowrap;
        // width: 100%;

        article {
            display: flex;
            justify-content: center;
            align-items: center;

            img{
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

    .carosel-prev-button,
    .carosel-next-button {
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