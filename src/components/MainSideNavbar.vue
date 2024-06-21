<script>
import { FontAwesomeIcon } from '../js/font-awesome';

export default {
    components:{
        FontAwesomeIcon
    },
    data(){
        return{
            
        }
    }
}
</script>

<template>
    <div class="sidenav rounded-start-2">
        <a href="#"><font-awesome-icon icon="fa-solid fa-ruler-combined" /></a>
        <a href="#"><font-awesome-icon icon="fa-solid fa-life-ring" /></a>
        <a href="#"><font-awesome-icon icon="fa-solid fa-book" /></a>
        <a href="#"><font-awesome-icon icon="fa-solid fa-cart-shopping" /></a>
    </div>
</template>

<style lang="scss" scoped>

.sidenav {
    height: auto;
    width: 50px;
    position: fixed;
    z-index: 1;
    top: 30%;
    right: 0;
    background-color: white;
    border: 2px solid black;
    display: flex;
    flex-direction: column;
    align-items: center;
}

.sidenav a {
    padding: .4rem;
    text-decoration: none;
    font-size: 25px;
    color: black;
    display: block;
}

a>i{
    font-weight: 600;
    font-size: 20px
}

// .sidenav a:hover {
    
// }

</style>