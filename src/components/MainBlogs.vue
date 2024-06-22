<script>
import BlogCard from './BlogCard.vue';
import { FontAwesomeIcon } from '../js/font-awesome';
import img1 from '../assets/img/artist-blog-03-480x352.jpeg';
import img2 from '../assets/img/artist-blog-01-480x352.jpg';

export default {
    components:{
        FontAwesomeIcon,
        BlogCard
    },
    data() {
        return {
            blogs:[{
                img: img1,
                author: 'artist',
                title: 'Brush Strokes Energize Trees in Paintings',
                date: 'May 15, 2020',
                views: '688 views'
            },
            {
                img: img2,
                author: 'artist',
                title: 'Pocket-Sized Notebooks Hold Miniature Paintings',
                date: 'May 15, 2020',
                views: '603 views'
            }],
            mostViewed:[{
                    title:'Become a Better Blogger: Content Planning'
                },
                {
                    title:'Promoting Your Online Business on Pinterest'
                },
                {
                    title:'Gamification and Game-Based Learning'
                },
                {
                    title:'Designing an Online Course from Expert\'s perspective'
                },
                {
                    title:'Why Online Courses Are the Future of Education'
                }
            ]
        }
    }
};
</script>

<template>        
    <section>
        <div class="my-container">
            <div class="d-flex justify-content-between">
                <div id="most-viewed" class="p-4">
                    <p>enjoyable insights</p>
                    <h2>
                        Most Viewed <span>Best Blog</span>
                    </h2>
                    <ul>
                        <li v-for="viewed in mostViewed">
                            <span><font-awesome-icon icon="fa-solid fa-right-long" /></span>{{ viewed.title }}
                        </li>
                    </ul>
                </div>
                <div id="card-section" class="d-flex">
                    <BlogCard v-for="blog in blogs" :blog="blog"/>
                </div>
            </div>
        </div>
    </section>
    

</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins.scss' as *;
    
section{
    padding: 5rem 0;
    background-color: #f5f1ed;
}

div>p:first-child{
    @include uppercase-text();
    color: #8c89a2;
}

div#most-wiewed{
    width: 40%;
}

h2{
    font-weight: 600;
    margin-bottom: 2rem;

        span{
            font-weight: 400;
            color: #20ad96;
        }
}

ul{
    padding: 0;

        span{
            margin-right: 1rem;
            font-size: 10px;
        }
    
        li{
            list-style-type: none;
            font-weight: 600;
            margin-bottom: 1rem;
        }
}

div#card-section{
    width: 60%;
}



</style>