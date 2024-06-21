<script>
import { FontAwesomeIcon } from '../js/font-awesome';
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
        <div class="my-container pe-5">
            <div class="mb-5 text-center">
                <p>stimulated to learn?</p>
                <h2>Featured Online Courses</h2>
            </div>
            <div>
                <div class="d-flex flex-wrap justify-content-between">
                    <article class="d-flex mb-3 rounded-1" v-for="course in onlineCourses">
                        <img class="rounded-circle object-fit-cover me-4" :src="course.img" alt="">
                        <div class="align-content-center">
                            <p v-if="course.price === 'Free'">
                                {{ course.price }} 
                            </p>
                            <p v-else>
                                {{ course.price }}<span class="decimal">.00</span>
                            </p>
                            <h5>
                                {{ course.title }}
                            </h5>
                            <div class="study">
                                <span>
                                    <span class="me-2"><font-awesome-icon icon="fa-regular fa-file-lines"/></span>
                                    <span>{{ course.lessons }}</span>
                                </span>
                                <span>
                                    <span class="me-2"><font-awesome-icon icon="fa-regular fa-user" /></span>
                                    <span>{{ course.students }}</span>
                                </span>
                            </div>
                        </div>
                    </article>
                </div>
            </div>
            <div class="d-flex justify-content-center p-2">
                <button class="px-5 py-2">View all courses &rightarrow;</button>
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

article{
    width: 550px;
    padding: 1.5rem;

        div>p{
            font-size: 25px;
            color: #20Ad96;
            font-weight: bold;

                span.decimal{
                    font-size: 20px;
                }
        }
}

article:hover{
    background-color: white;
}

img{
    width: 150px;
    height: 150px;
}

h5{
    font-weight: 600;
}

h5:hover{
    color: #20Ad96;
    cursor: pointer;
}

div.study>span{
    font-size: 14px;
    margin-right: 2rem;
    color: #8c89a2;
}

button{
    font-size: 14px;
    font-weight: bold;
    border: none;
    color: white;
    background-color: #20Ad96;
    border-radius: 5px;
}

</style>