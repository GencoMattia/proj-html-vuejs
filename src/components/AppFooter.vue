<script>
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';

export default {
    components: {
        FontAwesomeIcon,
    },
    data() {
        return {
            adressInfo: {
                address: '382 NE 191st St # 87394 Miami, FL 33179-3899',
                numberDate: '+1 (305) 547-9909 (9am - 5pm EST, Monday - Friday)',
                email: 'support@maxcoach.com'
            },
            exploreInfo: [
                {
                    link: 'Start here'
                },
                {
                    link: 'Blog'
                },
                {
                    link: 'About us'
                },
                
            ],
            exploreInfoNext: [
                {
                    link: 'Success story'
                },
                {
                    link: 'Courses'
                },
                {
                    link: 'Contact us'
                },
            ],
            InformationInfo: [
                {
                    link: 'Membership'
                },
                {
                    link: 'Purchase guide'
                },
                {
                    link: 'Privacy policy'
                },
                {
                    link: 'Terms of services'
                },
            ],
        };
    }
};
</script>

<template>
    <section class="footer-information">
        <div class="container my-container">
            <div class="row">
                <div class="col-6 addresses">
                    <h6 class="bold">
                        Address
                    </h6>
                    <p> {{ adressInfo.address }} </p>
                    <p> {{ adressInfo.numberDate }} </p>
                    <a href="">
                        {{ adressInfo.email }}
                    </a>
                </div>
                <div class="col-6 d-flex">
                    <div class="col-3 explore">
                        <h6>
                            Explore
                        </h6>
                        <a class="d-flex flex-wrap" href="" v-for="link in exploreInfo" :key="info">
                            {{ link.link }}
                        </a>
                        <font-awesome-icon icon="fa-brands fa-square-facebook" />
                    </div>
                    <div class="col-3 explore-next">
                        <h6></h6>
                        <a class="d-flex flex-wrap" href="" v-for="link in exploreInfoNext" :key="next">
                            {{ link.link }}
                        </a>
                    </div>
                    <div class="col-5 information">
                        <h6>
                            Information
                        </h6>
                        <a class="d-flex flex-wrap" href="" v-for="link in InformationInfo" :key="info">
                            {{ link.link }}
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
@use '../styles/general.scss' as *;

    .footer-information {
        background-color: #f8f8f8;
        padding: 69px 0px 50px 0px;
    }

            // adress
    div.addresses {
        font-size: 13px;
        color: #696969;

        p {
            padding-top: 0.50rem;
        }

        a {
            text-decoration: none;
            color: #696969;
            padding-top: 0.50rem;
            

            &:hover {
                color: #20ad96;
                transition: all 0.25s cubic-bezier(0.645, 0.045, 0.355, 1);
            }
        }

        
    }

    .explore,
    .explore-next,
    .information {
        
        a {
            text-decoration: none;
            color: #696969;
            font-size: 14px;
            padding-top: 1rem;

            &:hover {
                color: #20ad96;
                transition: all 0.25s cubic-bezier(0.645, 0.045, 0.355, 1);
            }
        }

    }

    .explore-next {
        padding-top: 1.1rem;
    }

    h6 {
            font-weight: 700;
            color: black;
    }
</style>