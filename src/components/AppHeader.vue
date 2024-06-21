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
                name: 'Home',
                image: './src/assets/images/homepages-mega-menu-image-alt.jpg',
                dropdown: [
                        {
                            name: 'MaxCoach Education'
                        },
                        {
                            name: 'Course Portal'
                        },
                        {
                            name: 'Distant Learning'
                        },
                        {
                            name: 'Multimedia Pedagogy'
                        },
                        {
                            name: 'Modern Schooling'
                        },
                        {
                            name: 'Remote Treaning'
                        },
                        {
                            name: 'Healt Coaching'
                        },
                        {
                            name: 'Gym Coaching'
                        },
                        {
                            name: 'Business'
                        },
                        {
                            name: 'Artist'
                        },
                        
                    ],
                    dropdownNext: [
                        {
                            name: 'Kitchen Coach'
                        },
                        {
                            name: 'Motivation'
                        },
                        {
                            name: 'Dancing'
                        },
                        {
                            name: 'Guitar'
                        },
                        {
                            name: 'Yoga'
                        },
                        {
                            name: 'Photography'
                        },
                        {
                            name: 'Personal Fiance'
                        },
                        {
                            name: 'Sales Coaching'
                        },
                        {
                            name: 'Mental Therapy'
                        },
                    ],
            },
            {
                name: 'Pages',
                dropdown: [
                        {
                            name: 'Start Here'
                        },
                        {
                            name: 'Success Story'
                        },
                        {
                            name: 'About Me'
                        },
                        {
                            name: 'About us 01'
                        },
                        {
                            name: 'About us 02'
                        },
                        {
                            name: 'About us 03'
                        },
                        {
                            name: 'Contact me'
                        },
                        {
                            name: 'Contact us'
                        },
                        {
                            name: 'Purchaise Guide'
                        },
                        {
                            name: 'Privacy Policy'
                        },
                        {
                            name: 'Terms of Service'
                        },
                ],
            },
            {
                name: 'Courses',
                dropdown: [
                {
                            name: 'Courses Grid 01'
                        },
                        {
                            name: 'Courses Grid 02'
                        },
                        {
                            name: 'Courses Grid 03'
                        },
                        {
                            name: 'Membership Level'
                        },
                        {
                            name: 'Become a Teacher'
                        },
                        {
                            name: 'Profile'
                        },
                        {
                            name: 'Checkout'
                        },
                        {
                            name: 'Single Layout'
                        },
                ],
            },
            {
                name: 'Features',
                dropdown: [
                    {
                        name: 'Events'
                    },
                    {
                        name: 'Zoom Meetings'
                    },
                ],
            },
            {
                name: 'Blog',
                dropdown: [
                    {
                        name: 'Blog Grid'
                    },
                    {
                        name: 'Blog Mansory'
                    },
                    {
                        name: 'Blog Classic'
                    },
                    {
                        name: 'Blog List'
                    },
                ],
            },
            {
                name: 'Shop',
                dropdown: [
                    {
                        name: 'Shop Left Sidebar'
                    },
                    {
                        name: 'Shop Right Sidebar'
                    },
                    {
                        name: 'Cart'
                    },
                    {
                        name: 'Wishlist'
                    },
                    {
                        name: 'SingleProduct'
                    },
                ]
            },
        ],
        list: 0,
        
        // imageHomePage: {
        //     image: './src/assets/images/homepages-mega-menu-image-alt.jpg',
        // },
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
            <div class="li-links" v-for="(link,index) in linksNav" :key="index" @click="list=(index)">
                <div class="dropdown">
                    <a class="dropdown-toggle border-green " href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false">
                        <span class="hover-underline-animation" >{{ link.name }}</span>
                    </a>
                    <ul class="dropdown-menu my-width" :class="index===0 ? 'position'  : ''">
                        <li class="d-flex justify-content-between">
                            <section class="d-flex my-padding">
                                <div class="links" :class="index===0 ? 'wide-panel'  : ''">
                                    <li v-for="(link, index) in linksNav[list].dropdown" :key="index">
                                        <a href=""> 
                                            <span>
                                                {{ link.name }}
                                            </span>
                                        </a>
                                    </li>
                                </div>
                                <div class="links-next" :class="index===0 ? 'small-panel' : ''">
                                    <li v-for="(link, index) in linksNav[list].dropdownNext" :key="index">
                                        <a href="">
                                            <span> 
                                                {{ link.name }}
                                            </span> 
                                        </a></li>
                                </div>
                                <div class="nav-img" :class="index===0 ? 'img-panel' : ''">
                                    <img :src="link.image" > 
                                </div>
                            </section>
                        </li> 
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

        // navbar
article {
    box-shadow: 5px 2px 5px #b9b9b9;
    position: sticky;
    top: 0;
    left: 0;
    right: 0;
    z-index: 2;
    background-color: white;


    .h-container {
        height: 80.4px;
        
        .logo {
            width: 25%;

            img {
            width: 158px;
    
            }

        }
            // hover
        a.border-green {
            color: #3d3d3d;
            
            &:hover {
                color: #20ad96;
                transition: all 0.25s cubic-bezier(0.645, 0.045, 0.355, 1);
            }
        }    

        .hover-underline-animation {
            display: inline-block;
            position: relative;
            color: #3d3d3d;
            font-weight: 200;

            &:hover {
                color: #20ad96;
                }
        }

        .hover-underline-animation:after {
            content: '';
            position: absolute;
            width: 100%;
            transform: scaleX(0);
            height: 2px;
            bottom: 0;
            left: 0;
            background-color: #20ad96;
            transform-origin: bottom right;
            transition: transform 0.25s ease-out;
        }

        .hover-underline-animation:hover:after {
            transform: scaleX(1);
            transform-origin: bottom left;
        }
        

    }
}
        // dropdown menu

.my-padding {
    padding: 1.5rem 1.5rem 0 1.5rem;
}

.nav-img {

    img {
        width: 100%;
    }
}

.position {
    position: absolute !important;
    left: -314px !important;
}

.img-panel {
    width: 546px;
}

.wide-panel {
    width: 300px;
}

.small-panel {
    width: 295px;
}

.dropdown-menu {
    border: collapse;
    border: 1px solid white;
    border-radius: 0px;    
    border-bottom: 4px solid #20ad96;
    padding: 0 !important;
    min-width: 11rem !important;

    div li a span{
        
        &:hover {
            color: #20ad96;
        }
    }
}

.my-width  {
    
    

    div.links li a ,
    div.links-next li a {
        text-decoration: none;
        color: #6c6c6c;
        font-size: 16px;
        font-weight: 200;
        margin-bottom: 2rem;

        
    }

    li {
        margin-bottom: 1rem;
    }
}
                // nav-links
div.dropdown > a {

    padding-top: 29px;
    padding-bottom: 29px;
    padding-left: 18px;
    padding-right: 18px;    
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
        background-color: #f5f5f5;
        border: 1px solid #f5f5f5;
        color: #20ad96;
        border-top-right-radius: 5px;
        border-bottom-right-radius: 5px;
        position: absolute;
        
        

        &:hover {
            color: white;
            background-color: #20ad96;
        }
    }

}






</style>