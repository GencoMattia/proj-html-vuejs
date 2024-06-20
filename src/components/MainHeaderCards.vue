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
            ]
        };
    },

    methods: {
        getImagePath: function(img) {
            return new URL(`../assets/img/${img}`, import.meta.url).href;
        }
    }
};
</script>

<template>
    <div class="my-container row"> 
        <div class="carosel-prev-button col-1">
            <button class="prev-card">
                <font-awesome-icon icon="chevron-left" />
            </button>
        </div>
        <div class="carosel-container col-10">
            <div class="carosel-row row">
                <article class="col-2" 
                v-for="(logo, index) in clientsCards" :key="index">
                    <img :src="getImagePath(logo.icon)" alt="client-logo">
                </article>
            </div>
        </div>
        <div class="carosel-next-button col-1">
            <button class="next-card">
                <font-awesome-icon icon="chevron-right" />
            </button>
        </div>
    </div>
</template>

<style scoped lang="scss">
@use "../styles/partials/mixins" as *;

    div {
        flex-wrap: nowrap;
        overflow: hidden;

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