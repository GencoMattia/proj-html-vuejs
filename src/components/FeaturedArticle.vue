<script>
import { FontAwesomeIcon } from '../js/font-awesome';

    export default {
        components:{
            FontAwesomeIcon
        },
        data(){
            return{
                
            }
        },
        props:{
            course:{
                type: Object,
                required: true
            }
        }
    }
</script>

<template>
<article class="d-flex mb-3 rounded-1" >
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
</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;

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

</style>