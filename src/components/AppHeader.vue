<script>
import { FontAwesomeIcon } from "../js/font-awesome";


export default {
    components: {
        FontAwesomeIcon,
        
    },
    data() {
        return {
        linksNav: [
            {
                name: 'Home'
            },
            {
                name: 'Pages'
            },
            {
                name: 'Courses'
            },
            {
                name: 'Features'
            },
            {
                name: 'Blog'
            },
            {
                name: 'Shop'
            },
        ]
        };
    }
};
</script>

<template>
    <article>
        <section class="my-container d-flex justify-content-around h-container
        align-items-center">
            <div class="logo">
                <a href=""> <img src="../assets/images/dark-logo.png" alt=""></a>
            </div>
            <div class="li-links" v-for="link in linksNav" :key="link">
                <div class="dropdown">
                    <a class="dropdown-toggle border-green" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false">
                        <span>{{ link.name }}</span>
                    </a>
                    <ul class="dropdown-menu">
                        <li><a class="dropdown-item" href="#">Action</a></li>
                        <li><a class="dropdown-item" href="#">Another action</a></li>
                        <li><a class="dropdown-item" href="#">Something else here</a></li>
                    </ul>
                </div>
            </div>
            <div class="search">
                <a href=""><font-awesome-icon icon="fa-regular fa-user" /></a>
                <input class="search-bar color-search" type="search" placeholder="    Search...">
                <button class="lent">
                    <font-awesome-icon icon="fa-solid fa-magnifying-glass" />
                </button>
            </div>
        </section>
    </article>
</template>

            
        

<style scoped lang="scss">


article {
    box-shadow: 5px 2px 5px #b9b9b9;
    position: fixed;
    width: 100%;


    .h-container {
        height: 80.4px;
        
        .logo {
            width: 25%;

            img {
            width: 158px;
    
            }

        }
            a.border-green {
                text-decoration: none;
                color: #3d3d3d;

                &:hover {
                    color: #20ad96;
                }

                span {

                    &:hover {
                        color: #20ad96;
                        border-bottom: 2px solid #20ad96;
                        
                    }
                }
            }
        

    }
}
                // nav-links
div.dropdown {
    a {
        padding-top: 29px;
        padding-bottom: 29px;
        padding-left: 18px;
        padding-right: 18px;
    }
}

                // Input
div.search {

                // profile-icon
    a {
        border: 2px solid black;
        border-radius: 25px;
        padding: 1px 3px;
        font-size: 11px;
        margin-right: 1rem;
        color: black;

        &:hover {
            color: #20ad96;
            border: 2px solid #20ad96;
        }
    }
        // search-bar
    .search-bar {
        min-height: 48px;
        padding-right: 50px;
        border-top-left-radius: 5px;
        border-bottom-left-radius: 5px;
        border: 1px solid #f5f5f5;
        background-color: #f5f5f5;
        color: #b8b8b8;
        max-width: 100%;
        width: 150px;
        
        

        .color-search {
            color: #696969;
            border-color: #f5f5f5;
            background: #f5f5f5;
        }
        
    }
        // lenth-icon
    .lent {
        min-height: 48px;
        padding-right: 17.5px;
        padding-left: 17.5px;
        background-color: white;
        border: 1px solid white;
        color: #20ad96;
        border-top-right-radius: 5px;
        border-bottom-right-radius: 5px;
        
        

        &:hover {
            color: white;
            background-color: #20ad96;
        }
    }

}






</style>