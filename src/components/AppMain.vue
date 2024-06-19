<script>
import MainHeader from './MainHeader.vue';
import MainHeaderCards from './MainHeaderCards.vue';
import MainFeatured from './MainFeatured.vue';
import MainBenefits from './MainBenefits.vue';
import MainGuide from './MainGuide.vue';
import MainTopLearners from './MainTopLearners.vue';
import MainGetStarted from './MainGetStarted.vue';
import MainStatistics from './MainStatistics.vue';
import MainBlogs from './MainBlogs.vue';
import MainNewsletter from './MainNewsletter.vue';

export default {
    components: {
        MainHeader,
        MainHeaderCards,
        MainFeatured,
        MainBenefits,
        MainGuide,
        MainTopLearners,
        MainGetStarted,
        MainStatistics,
        MainBlogs,
        MainNewsletter,
    },

    data() {
        return {
        
        };
    }
};
</script>

<template>
    <MainHeader />
    <MainHeaderCards />
    <MainFeatured />
    <MainBenefits />
    <MainGuide />
    <MainTopLearners />
    <MainGetStarted />
    <MainStatistics />
    <MainBlogs />
    <MainNewsletter />



    <h1>
        Io Sono un Main!
    </h1>
</template>

<style scoped lang="scss">

</style>