<script>
import axios from 'axios';
import { FontAwesomeIcon } from '../js/font-awesome';

export default {
    components: {
        FontAwesomeIcon 
    },
    
    data() {

        return {
            eventsList: [

            ],
        };
    },

    methods: {
        fetchEvents() {
            axios.get('http://152.89.170.170:3000/events/elearning')
            .then((response) => {
                console.log(response.data);
                this.eventsList = response.data;
            })
            .catch((error) => {
                console.error("Error fetching events:", error);
            });
        }
    },

    mounted() {
        this.fetchEvents();
    }
};
</script>

<template>
    <main>
        <div class="my-container">
            <section class="main_events"> 
                <div class="page-path">
                    <p class="m-0">
                        home  /  event
                    </p>
                </div>
                <div class="page-title text-center">
                    <h1>
                        Events
                    </h1>
                </div>
                <div class="events-filter d-flex justify-content-between mb-4">
                    <p class="available-events">
                        We found <span class="available-events-num">{{ eventsList.length }}</span> events available for you
                    </p>
                    <select class="form-select form-select-lg mb-3" aria-label="Large select example">
                        <option selected>Open this select menu</option>
                        <option value="1">One</option>
                        <option value="2">Two</option>
                        <option value="3">Three</option>
                    </select>
                </div>
                <div class="events-cards-wrapper">
                    <div class="card border-0" style="width: 18rem;" v-for="(event, index) in eventsList" :key="index">
                        <img :src="event.image" class="card-img-top" alt="...">
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
                </div>
            </section>
        </div>
    </main>
</template>

<style scoped lang="scss">
@use "../styles/partials/mixins" as *;

    .page-title {
        padding: 5rem;

        h1 {
            font-weight: bolder;
        }
    }

    .events-filter {

        .available-events{
            color: #7e7e7e;

            .available-events-num {
                color: black;
                font-weight: bold;
            }
        }

        select {
            width: 15rem;
            font-size: 1rem;
        }
    }
    

    .events-cards-wrapper {
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
        width: 100%;

        .card {
            width: calc((100% / 3) - 1.5rem) !important;
            margin-bottom: 2rem;
            text-align: center;
            display: flex;

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
    }

</style>