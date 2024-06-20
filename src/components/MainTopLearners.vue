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
    <section class="testimonials row overflow-hidden align-items-stretch justify-content-evenly">
        <article v-for="(card, index) in visibleCards" :key="index" @click=""
        class="testimonal-card col-3 p-5 d-flex flex-column justify-content-between">
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
                <div class="testimonial-info">
                    <p class="testimonial-name">
                        {{ card.name }}
                    </p>
                    <p class="testimonial-occupation">
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
                :class="{ 'active-circle': learnersList.indexOf(card) === activeArticle }"
            />
        </div>
    </section>
</template>

<style scoped lang="scss">
@use "../styles/partials/mixins" as *;

    article {
        background-color: lightcyan;
        margin-bottom: 7rem;
    }

    .carosel-circles {
        color: #b7b5c4;

        .active-circle {
            color: #3f3a64;
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