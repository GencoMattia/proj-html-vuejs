<script>
import { FontAwesomeIcon } from '../js/font-awesome';

export default {
    components: {
        FontAwesomeIcon,
    },

    data() {
        return {
        
        };
    },

    props: {
        event: {
            type: Object,
            required: true,
        }
    }
};
</script>

<template>
    <div class="card border-0" style="width: 18rem;">
        <div class="image-container">
            <img :src="event.image" class="card-img-top" alt="...">
            <div class="overlay">
                <button>
                    Get ticket
                </button>
            </div>
        </div>
        <div class="card-body d-flex flex-column justify-content-between">
            <p class="card-text event-date">
                {{ event.start_date }}
            </p>
            <p class="card-text event-name">
                {{ event.event_name }}
            </p>
            <p class="card-text event-location">
                <font-awesome-icon icon="location-dot" /> {{ event.location }}
            </p>
        </div>
    </div>
</template>

<style scoped lang="scss">
@use "../styles/partials/mixins" as *;

    .card {
        width: calc((100% / 3) - 1.35rem) !important;
        margin-bottom: 2rem;
        text-align: center;
        display: flex;
        overflow: hidden;

        &:hover img{
            transform: scale(1.1);
        }

        &:hover .overlay {
            opacity: 1 !important;
        }

        .image-container {
            overflow: hidden;
            position: relative;

            .overlay {
                @include flex-centered;
                position: absolute;
                top: 0;
                left: 0;
                right: 0;
                bottom: 0;
                background-color: rgba(63,58,100,0.6);
                opacity: 0;
                transition: opacity 0.3s ease;

                button {
                    font-weight: bolder;
                    color: #20ad96;
                    border: none;
                    padding: .5rem 2rem;
                    border-radius: .5rem;
                }
            }

            .card-img-top {
                transition: transform 0.6s ease;
            }
        }

        .event-date {
            color: #20ad96;
            @include uppercase-text;
            font-weight: bold;
        }

        .event-name {
            font-weight: bold;
            font-size: 1.2rem;
        }

        .event-location {
            color: #7e7e7e;
        }
    }
</style>