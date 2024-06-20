<script>
import img1 from '../assets/img/home-2-image-box-01.png';
import img2 from '../assets/img/about-us-02-image-box-02.png'
import img3 from '../assets/img/home-2-image-box-03.png'
export default {
    data() {
        return {
            benefits: [{
                img: img1,
                title: 'Customize Preferences',
                paragraph: 'Learners are given the right to arrange and customize their study schedule and timetable based on preferences.',
                link: 'Start here'
            },
            {
                img: img2,
                title: 'Cloud Storage',
                paragraph: 'You can store online lessons via online cloud or download to your device and revise lessons on the way.',
                link: 'Get Free Quote'
            },
            {
                img: img3,
                title: 'Multimedia Channels',
                paragraph: 'We provide study materials with various formats: video, audio, slides, doc, prints, books and applications.',
                link: 'Start now'
            }]
        };
    }
};
</script>

<template>
    <section>
        <div>
            <p>
                maxcoach available courses
            </p>
            <h2>
                Access <span>Smart Tutoring</span> Program For Benefits.
            </h2>
        </div>
        <div>
            <article v-for="benefit in benefits">
                <img :src="benefit.img" alt="">
                <div>
                    <h3>
                        {{ benefit.title }}
                    </h3>
                    <p>
                        {{ benefit.paragraph }}
                    </p>
                    <a href="#">
                        {{ benefit.link }} <span>&rightarrow;</span>
                    </a>
                </div>
            </article>
        </div>
    </section>

</template>

<style lang="scss" scoped>

</style>