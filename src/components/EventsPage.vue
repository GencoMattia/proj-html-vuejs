<script>
import axios from 'axios';

export default {
    data() {
        return {
        
        };
    },

    methods: {
        fetchEvents() {
            axios.get('http://152.89.170.170:3000/events/elearning')
                .then((response) => {
                    console.log(response.data);
                    this.events = response.data;
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

</template>

<style scoped>

</style>