<script>
import { FontAwesomeIcon } from '../js/font-awesome';

export default {
    components: {
        FontAwesomeIcon,
    },

    data() {
        return {
            learnersList: [
                {
                    avatar:"testimonial-avata-02.jpg",
                    name: "Mina Hollace",
                    occupation: "Freelancer",
                    title: "High level of efficiency and scientific teaching methods",
                    text: "I am free to learn at my own pace, follow my own schedule and choose the subject I want to learn from the syllabus. Great study portal for people like me.",
                    isVisible: false,
                },
                {
                    avatar:"testimonial-avata-04.jpg",
                    name: "Madley Pondor",
                    occupation: "IT Specialist",
                    title: "Professional team of specialists and passionate mentors at reach",
                    text: "I need to get a certification for English proficiency and MaxCoach is my best choice. Their tutors are smart and professional when dealing with students.",
                    isVisible: false,
                },
                {
                    avatar:"testimonial-avata-01.jpg",
                    name: "Luvic Dubble",
                    occupation: "Private Tutor",
                    title: "The MaxCoach team works really hard to ensure high quality",
                    text: "I am happy with thir arrangement of lessons and subjects. They reflect a scientific investigation into effective methods to be adopted for learners of all levels.",
                    isVisible: false,
                },
                {
                    avatar:"testimonial-avata-03.jpg",
                    name: "Florence Themes",
                    occupation: "Multimedia Admin",
                    title: "It's a choice of quality for people with special needs",
                    text: "I'm a very scrict person so I require everything to be organized and neat. Then, I'll be able to make things right and shine. MaxCoach guys just got me.",
                    isVisible: false,
                },

            ],

            activeArticle: 0,
        };
    },

    methods: {
        getImagePath: function(img) {
            return new URL(`../assets/img/${img}`, import.meta.url).href;
        },

        setActiveCircle(variable, index) {
            variable = index;
        },

        getSideActiveClass(index) {
            return index === this.activeArticle - 1 || index === this.activeArticle + 1;
        }
    },

    computed: {
        visibleCards() {
            const index = this.activeArticle;
            const count = this.learnersList.length;

            const prevIndex = (index - 1 + count) % count;
            const nextIndex = (index + 1) % count;

            return [
                this.learnersList[prevIndex],
                this.learnersList[index],
                this.learnersList[nextIndex]
            ];
        }
    }
};
</script>

<template>
    <section class="introduction d-flex justify-content-center">
        <div class="title">
            <h6 class="center color-grey">
                great words about maxcoach
            </h6>
            <h2>
                Our <span class="color-green weight">top leaners'</span> verbatim
            </h2>
        </div>
    </section>
    <section class="testimonials row overflow-hidden align-items-stretch justify-content-evenly">
        <article v-for="(card, index) in visibleCards" :key="index" @click="activeArticle = learnersList.indexOf(card)"
        class="testimonal-card col-3 p-5 d-flex flex-column justify-content-between"
        :class="{ 'side-active': index !== 1 }">
            <div class="card-content">
                <h2>
                    {{ card.title }}
                </h2>
                <p>
                    {{ card.text }}
                </p>
            </div>
            <div class="card-profile d-flex align-items-center">
                <div class="testimonial-picture me-4">
                    <img :src="getImagePath(card.avatar)" :alt="`{{ card.name }}-img`">
                </div>
                <div class="testimonial-info d-flex flex-column justify-content-between">
                    <p class="testimonial-name">
                        {{ card.name }}
                    </p>
                    <p class="testimonial-occupation m-0">
                        / {{ card.occupation }}
                    </p>
                </div>
            </div>
        </article>
        <div class="carosel-circles d-flex justify-content-center gap-3">
            <font-awesome-icon 
                v-for="(card, index) in learnersList" 
                :key="index" 
                @click="activeArticle = index"
                icon="fa-solid fa-circle" 
                :class="{ 'active-circle': index === activeArticle }"
            />
        </div>
    </section>
</template>

<style scoped lang="scss">
@use "../styles/partials/mixins" as *;

            // sezione titolo
    .introduction {
        padding: 3rem 0;
    }

    .center {
        text-align: center;
    }

    h2 {
        color: #3f3a64;
        font-weight: 600;

        .color-green {
            color: #20ad96;
            font-weight: 400

        }
    }

    
    section.testimonials {
        padding-bottom: 1rem;
    }
    

    .color-grey {
        @include uppercase-text();
        color: #8d8aa3;
        font-weight: 300;
    }

    .weight {
        font-weight: 200;
    }
            // fine sezione titolo
    section {
        background-color: #f8f8f8;
        width: 100%;
    }

    article {
        background-color: white;
        margin-bottom: 7rem;
        border-radius: 5px;
        height: 430px;
    }

    .side-active {
        opacity: .5;
    }
    
    .carosel-circles {
        color: #b7b5c4;
        font-size: .5rem;

        transition: transform 0.3s ease;

        .active-circle {
            color: #3f3a64;
            transform: scale(1.5);
        }
    }

    .testimonial-picture {
        width: 75px;

        img {
            width: 100%;
            border-radius: 50%;
        }
    }

    .card-content {
        h2 {
            font-size: 1rem;
            font-weight: bolder;
        }
    }

    .testimonial-name {
        @include uppercase-text;
        font-weight: bold;
        font-size: .9rem;
    }

    .testimonial-occupation {
        color: #979797;
        font-size: .8rem;
    }
</style>