<script>
import FeaturedArticle from './FeaturedArticle.vue';
import { FontAwesomeIcon } from '../js/font-awesome';
import img1 from '../assets/images/course-02-480x298.jpg';
import img2 from '../assets/images/stock-full-hd-03-480x298.jpg';
import img3 from '../assets/images/stock-full-hd-04-480x298.jpg';
import img4 from '../assets/images/stock-full-hd-06-480x298.jpg';
import img5 from '../assets/images/course-featured-image-01-480x298.jpg';
import img6 from '../assets/images/stock-full-hd-05-480x298.jpg';

export default {
    components:{
        FontAwesomeIcon,
        FeaturedArticle
    },
    data() {
        return {
            onlineCourses:[{
                img: img1,
                price: '$40',
                title: 'Learning to write as a Professional Author',
                lessons: '20 Lessons',
                students: '50 Students'
            },
            {
                img: img2,
                price: 'Free',
                title: 'Customer-centric Info-Tech Strategies',
                lessons: '24 Lessons',
                students: '769 Students'
            },
            {
                img: img3,
                price: '$19',
                title: 'Open Programming Courses for Everyone: Python',
                lessons: '17 Lessons',
                students: '62 Students'
            },
            {
                img: img4,
                price: '$26',
                title: 'Accademic Listening and Note-taking',
                lessons: '14 Lessons',
                students: '67 Students'
            },
            {
                img: img5,
                price: '$39',
                title: 'Master jQuery in a Short Period of Time',
                lessons: '6 Lessons',
                students: '51 Students'
            },
            {
                img: img6,
                price: '$59',
                title: 'Introduction to Javascript for Beginners',
                lessons: '14 Lessons',
                students: '76 Students'
            }],
        };
    }
};
</script>

<template>
    <section>
        <div class="my-container pe-5">
            <div class="mb-5 text-center">
                <p>stimulated to learn?</p>
                <h2>Featured Online Courses</h2>
            </div>
            <div>
                <div class="d-flex flex-wrap justify-content-between">
                    <FeaturedArticle v-for="course in onlineCourses" :course="course"/>
                </div>
            </div>
            <div class="d-flex justify-content-center p-2">
                <button class="px-5 py-2">View all courses <font-awesome-icon icon="fa-solid fa-arrow-right" /></button>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;

section{
    background-color: #f5f7fa;
    padding: 5rem 0;
}

div.text-center>p{
    @include uppercase-text();
    color: #8c89a2;
}

h2{
    font-weight: 600;
}

button{
    @include button-style();

    transition: all .3s ease;

    &:hover {
        background-color: #3f3a64;
    }
}

</style>