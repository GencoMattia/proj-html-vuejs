<script>
import axios from 'axios';

export default {
    data() {
        return {
            eventsList: [

            ]
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

                </div>
                <div class="page-title">

                </div>
                <div class="events-filter">

                </div>
                <div class="events-cards-wrapper">
                    <div class="card" style="width: 18rem;">
                        <img src="..." class="card-img-top" alt="...">
                        <div class="card-body">
                            <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
                        </div>
                    </div>
                </div>
            </section>
        </div>
    </main>
</template>

<style scoped lang="scss">

</style>