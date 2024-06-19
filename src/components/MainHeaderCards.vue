<script>
export default {
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
    <div class="my-container"> 
        <article v-for="(logo, index) in clientsCards" :key="index">
            <img :src="getImagePath(logo.icon)" alt="client-logo">
        </article>
    </div>
</template>

<style scoped lang="scss">

</style>