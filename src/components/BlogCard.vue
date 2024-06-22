<script>
import { FontAwesomeIcon } from '../js/font-awesome';

    export default {
        components:{
            FontAwesomeIcon,
        },
        data(){
            return{
                
            }
        },
        props:{
            blog:{
                type: Object,
                required: true
            }
        }
    }
</script>

<template>
<div class="card">
    <div class="image-container">
        <img class="card-img-top" :src="blog.img" alt="image">
    </div>
    <div class="card-body py-4">
        <p>
            {{ blog.author }}
        </p>
        <h5>
            {{ blog.title }}
        </h5>
        <span class="date">
            <span><font-awesome-icon icon="fa-regular fa-calendar" /></span>
            <span>{{ blog.date }}</span>
        </span>
        <span class="views">
            <span><font-awesome-icon icon="fa-regular fa-eye" /></span>
            <span>{{ blog.views }}</span>
        </span>
    </div>
</div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;

div.card{
    max-width: 300px;
    margin-left: 3rem;
}

div.image-container{
    overflow: hidden;

        img{
            transition: transform 0.6s ease;

            &:hover{
                @include scaling-hover;
            }
        }
}

div>p:first-child{
    @include uppercase-text();
    color: #8c89a2;
}

h5{
    font-weight: 600;
    margin-bottom: 1.5rem;
}

span.date,
span.views{
    margin-right: 1.3rem;
}

span.date>span,
span.views>span{
    font-size: 14px;
    margin-right: .5rem;
    color: #8c89a2;
}

</style>