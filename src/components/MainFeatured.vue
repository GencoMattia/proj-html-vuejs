<script>
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';
import img1 from '../assets/images/course-02-480x298.jpg';
import img2 from '../assets/images/stock-full-hd-03-480x298.jpg';
import img3 from '../assets/images/stock-full-hd-04-480x298.jpg';
import img4 from '../assets/images/stock-full-hd-06-480x298.jpg';
import img5 from '../assets/images/course-featured-image-01-480x298.jpg';
import img6 from '../assets/images/stock-full-hd-05-480x298.jpg';

export default {
    components:{
        FontAwesomeIcon
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
        <div>
            <p>stimulated to learn?</p>
            <h2>Featured Online Courses</h2>
        </div>
        <div>
            <article v-for="course in onlineCourses">
                <img :src="course.img" alt="">
                <div>
                    <p v-if="course.price === 'Free'">
                        {{ course.price }} 
                    </p>
                    <p v-else>
                        {{ course.price }} <span>.00</span>
                    </p>
                    <h3>
                        {{ course.title }}
                    </h3>
                    <span>
                        <font-awesome-icon icon="file-lines" /> {{ course.lessons }}
                    </span>
                    <span>
                        <font-awesome-icon icon="user" /> {{ course.students }}
                    </span>
                </div>
            </article>
        </div>
        <div>
            <button>View all courses &rightarrow;</button>
        </div>
    </section>

</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;

section>div>p{
    @include uppercase-text()
}




</style>