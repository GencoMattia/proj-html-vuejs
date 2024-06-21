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
import MainSideNavbar from './MainSideNavbar.vue';

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
        MainSideNavbar
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
    <MainSideNavbar />
</template>

<style scoped lang="scss">

</style>