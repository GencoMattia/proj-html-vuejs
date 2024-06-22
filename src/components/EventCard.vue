<script>
export default {
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

<style scoped>

</style>