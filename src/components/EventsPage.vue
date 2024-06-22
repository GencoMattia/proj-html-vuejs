<script>
import axios from 'axios';
import { FontAwesomeIcon } from '../js/font-awesome';
import EventCard from "./EventCard.vue";

import { store } from "../store";

export default {
    components: {
        FontAwesomeIcon,
        EventCard,
    },
    
    data() {

        return {
            eventsList: [

            ],

            eventsTypeList: [

            ],

            selectedType: "all",
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

        getPressedLink(link) {
            store.pressedLink = link;
            console.log(`Hai premuto ${store.pressedLink}`);
        }
    },

    computed: {
        filteredEventsList() {
            if (this.selectedType === 'all') {
                return this.eventsList; 
            } else {
                return this.eventsList.filter(event => event.type === this.selectedType);
            }
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
                        <a href="#" @click="getPressedLink('AppMain')">Home</a>  /  Event
                    </p>
                </div>
                <div class="page-title text-center">
                    <h1>
                        Events
                    </h1>
                </div>
                <div class="events-filter d-flex justify-content-between align-items-center mb-4">
                    <p class="available-events">
                        We found <span class="available-events-num">{{ filteredEventsList.length }}</span> events available for you
                    </p>
                    <div class="select-container d-flex align-items-center">
                        <label for="event-type" class="form-label m-0">
                            Event Type:
                        </label>
                        <select v-model="selectedType" @change="filterEventsByType" class="form-select form-select-lg border-0" aria-label="Large select example" id="event-type">
                            <option v-for="(type, index) in eventsTypeList" :value="type">
                                {{ type }}
                            </option>
                        </select>
                    </div>
                </div>
                <div class="events-cards-wrapper">
                    <EventCard  v-for="(event, index) in filteredEventsList" :key="index" :event="event"/>
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
            font-weight: 700;
            font-size: 3rem
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
        gap: 2rem;
        flex-wrap: wrap;
        width: 100%;
    }

</style>