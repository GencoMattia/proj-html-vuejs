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

            eventsTypeList: [

            ],
        };
    },

    methods: {
        fetchEvents() {
            axios.get('http://152.89.170.170:3000/events/elearning')
            .then((response) => {
                console.log(response.data);
                const events = response.data;
                const typeList = [
                    "all",
                ];

                events.forEach(singleEvent => {
                    if (singleEvent.type && !typeList.includes(singleEvent.type)) { 
                        typeList.push(singleEvent.type);
                    }
                });

                this.eventsList = events;
                this.eventsTypeList = typeList;
            })

            .catch((error) => {
                console.error("Error fetching events:", error);
            });
        },

        getEventsType() {

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
                <div class="events-filter d-flex justify-content-between align-items-center mb-4">
                    <p class="available-events">
                        We found <span class="available-events-num">{{ eventsList.length }}</span> events available for you
                    </p>
                    <div class="select-container d-flex align-items-center">
                        <label for="event-type" class="form-label m-0">
                            Event Type:
                        </label>
                        <select class="form-select form-select-lg border-0" aria-label="Large select example" id="event-type">
                            <option v-for="(type, index) in eventsTypeList" :value="index">
                                {{ type }}
                            </option>
                        </select>
                    </div>
                </div>
                <div class="events-cards-wrapper">
                    <div class="card border-0" style="width: 18rem;" v-for="(event, index) in eventsList" :key="index">
                        <div class="image-container">
                            <img :src="event.image" class="card-img-top" alt="...">
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

        .select-container {
            width: 15rem;
            font-size: 1rem;

            select {
                width: 65%;
                font-size: 1rem;

                &:focus {
                    box-shadow: 0 0 0 0.25rem rgba(39, 234, 11, 0.25);
                }
            }
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
            overflow: hidden;

            .image-container {
                overflow: hidden;

                .card-img-top {
                    transition: transform 0.6s ease;

                    &:hover {
                        transform: scale(1.1);
                    }
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
    }

</style>