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
    padding: .4rem 0;
    height: auto;
    width: 50px;
    position: fixed;
    z-index: 3;
    top: 30%;
    right: 0;
    background-color: white;
    box-shadow: 2px 1px 1px 3px #b9b9b9;
    display: flex;
    flex-direction: column;
    align-items: center;
}

.sidenav a {
    padding: .4rem;
    text-decoration: none;
    font-size: 17px;
    color: black;
    display: block;
}

.sidenav a:hover {
    background:#3f3a64;
    color:white;
}

</style>