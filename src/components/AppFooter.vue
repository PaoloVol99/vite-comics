<script>
import AppBonusComponent from './AppBonusComponent.vue'

export default {
    components: {
        AppBonusComponent,
    },
    data() {
        return {
            dcComics: [
                'Characters',
                'Comics',
                'Movies',
                'TV',
                'Games',
                'Videos',
                'News'
            ],
            shop: [
                'Shop DC',
                'Shop DC Collectibles'
            ],
            dc: [
                'Terms Of Use',
                'Privacy Policy (New)',
                'Ad Choices',
                'Advertising',
                'Jobs',
                'Subscriptions',
                'Talent Workshops',
                'CPSC Certificates',
                'Ratings',
                'Shop Help',
                'Contact Us'
            ],
            sites: [
                'DC',
                'MAD Magazine',
                'DC Kids',
                'DC Universe',
                'DC Power Visa'
            ]
        }
    }

}
</script>

<template>
    <footer>
        
        <AppBonusComponent />
    
        <div class="footer-main">
            <div class="container">
                <div class="col">
                    <div class="footer-links-wrapper">
                        <div class="col">
                            <h3>dc comics</h3>
                            <ul>
                                <li v-for="element in dcComics"> {{ element }}</li>
                            </ul>
                            <h3>shop</h3>
                            <ul>
                                <li v-for="element in shop">{{ element }}</li>
                            </ul>
                        </div>
                        <div class="col">
                            <h3>dc</h3>
                            <ul>
                                <li v-for="element in dc">{{ element }}</li>
                            </ul>
                        </div>
                        <div class="col">
                            <h3>sites</h3>
                            <ul>
                                <li v-for="element in sites">{{ element }}</li>
                            </ul>
                        </div>
                    </div>
                </div>
                <div class="col">
                    <img src="/img/dc-logo-bg.png" alt="">
                </div>
            </div>
        </div>
        <div class="footer-end">
            <div class="container">
                <div class="footer-socials">
                    <button>sign-up now!</button>
                    <div class="socials-wrapper">
                        <span class="follow">follow us</span>
                        <img src="/img/footer-facebook.png" alt="">
                        <img src="/img/footer-twitter.png" alt="">
                        <img src="/img/footer-youtube.png" alt="">
                        <img src="/img/footer-pinterest.png" alt="">
                        <img src="/img/footer-periscope.png" alt="">
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables' as*;

.footer-main {
    background-image: url(/img/footer-bg.jpg);
    padding: 24px 0;
    overflow: hidden;


    .container {
        display: flex;
        justify-content: space-between;

        .col {

            img {
                margin: -100px 0;
            }
            .footer-links-wrapper {
                display: flex;
                gap: 26px;

                .col {
                    h3 {
                        color: white;
                        text-transform: uppercase;
                        margin: 14px 0;
                        font-weight: 600;
                        font-size: 18px;
                    }
                    li {
                        color: grey;
                        line-height: 24px;
                        font-size: 12px;
                    }
                }
            }
        }
    }
}

.footer-end {
    background-color: $dc-grey;
    padding: 20px 0;

    .footer-socials {
        display: flex;
        justify-content: space-between;
        align-items: center;

        button {
            border: 2px solid $dc-blue;
            background-color: transparent;
            color: white;
            padding: 0 10px;
            line-height: 40px;
            text-transform: uppercase;
        }

        .socials-wrapper {
            display: flex;
            align-items: center;
            gap: 20px;

            img {
            width: 30px;
            }
            .follow {
                color: $dc-blue;
                text-transform: uppercase;
                font-weight: 600;
            }
        }
        
    }
}

</style>