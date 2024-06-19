<script>
export default {
    data() {
        return {
            learnersList: [
                {
                    avatar:"testimonial-avata-01.jpg",
                    name: "Mina Hollace",
                    occupation: "Freelancer",
                    title: "High level of efficiency and scientific teaching methods",
                    text: "I am free to learn at my own pace, follow my own schedule and choose the subject I want to learn from the syllabus. Great study portal for people like me.",
                },
                {
                    avatar:"testimonial-avata-02.jpg",
                    name: "Madley Pondor",
                    occupation: "IT Specialist",
                    title: "Professional team of specialists and passionate mentors at reach",
                    text: "I need to get a certification for English proficiency and MaxCoach is my best choice. Their tutors are smart and professional when dealing with students.",
                },
                {
                    avatar:"testimonial-avata-03.jpg",
                    name: "Luvic Dubble",
                    occupation: "Private Tutor",
                    title: "The MaxCoach team works really hard to ensure high quality",
                    text: "I am happy with thir arrangement of lessons and subjects. They reflect a scientific investigation into effective methods to be adopted for learners of all levels.",
                },
                {
                    avatar:"testimonial-avata-04.jpg",
                    name: "Florence Themes",
                    occupation: "Multimedia Admin",
                    title: "It's a choice of quality for people with special needs",
                    text: "I'm a very scrict person so I require everything to be organized and neat. Then, I'll be able to make things right and shine. MaxCoach guys just got me.",
                },
            ]
        };
    }
};
</script>

<template>
    <section class="testimonials row flex-nowrap overflow-hidden">
        <article v-for="(card, index) in learnersList" :key="index" class="testimonal-card col-4">
            <div class="card-content">
                <h2>
                    {{ card.title }}
                </h2>
                <p>
                    {{ card.text }}
                </p>
            </div>
            <div class="card-profile">

            </div>
        </article>
    </section>
</template>

<style scoped>

</style>