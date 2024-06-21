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
        <div class="my-container">
            <div class="text-center mb-5">
                <p>
                    maxcoach available courses
                </p>
                <h2>
                    Access <span>Smart Tutoring</span> Program For Benefits.
                </h2>
            </div>
            <div class="d-flex">
                <article class="p-4 me-3" v-for="benefit in benefits">
                    <img class="mb-3" :src="benefit.img" alt="">
                    <div>
                        <h4 class="mb-3">
                            {{ benefit.title }}
                        </h4>
                        <p>
                            {{ benefit.paragraph }}
                        </p>
                        <a href="#">
                            <span class="me-1">{{ benefit.link }}</span><span class="arrow">&rightarrow;</span>
                        </a>
                    </div>
                </article>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;

div>p:first-child{
    @include uppercase-text();
    color: #8c89a2;
}

h2{
    font-weight: 600;

        span{
            color: #20ad96;
            font-weight: 400;
        }
}

article{
    width: calc((100% / 3) - 1rem);
    
        h4{
            font-weight: 600;
        }

        p{
            font-size: 15px
        }
}

article:hover{
    cursor: pointer;

        a{
            color: #20ad96;
        }
}

a{
    text-decoration: none;
    font-weight: bold;
    color: #8c89a2;
    position: relative;

        span.arrow{
            font-size: 20px;
        }
}

a::after {
    content: '';
    position: absolute;
    height: 1px;
    left: 0;
    bottom: -.5rem;
    width: 0;
    background: lightgrey;
    transition: width .5s;
}

a:hover::after {
    width: 100%;
}


</style>