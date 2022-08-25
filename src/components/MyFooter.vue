<template>
    <footer>
            <div class="wrapper-top">
                <div class="container">
                    <ul>
                        <li v-for="(linkfooter, indice) in linkfoot" :key="indice">
                            <div class="wrapper-link">
                                <div class="img_link">
                                    <img :src="linkfooter.img" alt="">
                                </div>
                                <a :href="linkfooter.direzione">{{linkfooter.nome}}</a>
                            </div>
                        </li>
                    </ul>

                </div>
            </div>

            <div class="wrapper-mid">
                <div class="container">
                    <div class="cols">
                        <div class="col">
                            <MyCols :urls="dcComics" :titolo="'DC COMICS'" />
                            
                            <MyCols :urls="dc" :titolo="'DC'" />

                            <MyCols :urls="sites" :titolo="'SITES'" />

                            
                        </div>

                        <div class="col-img">
                            <img src="../assets/dc-logo-bg.png">
                        </div>
                    </div>
                </div>
            </div>


            <div class="wrapper-bot">
                <div class="container">

                    <div class="wrapper-footer-bot">

                        <button class="btn">SIGN-UP NOW!</button>

                        <div class="social">
                            <h2>FOLLOW AS</h2>
                            <img v-for="(social, indice) in social" :key="indice" :src="social.url" :alt="social.nome">
                        </div>
                    </div>
                    
                </div>
            </div>
    </footer>
</template>

<script>
import MyCols from './MyCols'

export default {
    nome: 'MyFooter',
    components:{
        MyCols,
    },
    data(){
        return{
            linkfoot:   [
                            {
                                nome: 'DIGITAL COMICS',
                                direzione: '#',
                                img: require ('../assets/buy-comics-digital-comics.png')
                            },
                            {
                                nome: 'DC MERCHANDISE',
                                direzione: '#',
                                img: require ('../assets/buy-comics-merchandise.png')
                            },
                            {
                                nome: 'SUBSCRIPTION',
                                direzione: '#',
                                img: require ('../assets/buy-comics-subscriptions.png')
                            },
                            {
                                nome: 'COMIC SHOP LOCATOR',
                                direzione: '#',
                                img: require ('../assets/buy-comics-shop-locator.png')
                            },
                            {
                                nome: 'DC POWER VISA',
                                direzione: '#',
                                img: require ('../assets/buy-dc-power-visa.svg')
                            },
                        ],

            dcComics:   [
                            {
                                voce: 'Characters',
                                url:'#'
                            },
                            {
                                voce: 'Comics',
                                url:'#'
                            },
                            {
                                voce: 'Movies',
                                url:'#'
                            },
                            {
                                voce: 'TV',
                                url:'#'
                            },
                            {
                                voce: 'Games',
                                url:'#'
                            },
                            {
                                voce: 'Videos',
                                url:'#'
                            },
                            {
                                voce: 'News',
                                url:'#'
                            },

                        ],
            shop:       [
                            {
                                voce: 'Shop DC',
                                url:'#'
                            },
                            {
                                voce: 'Shop DC Collectibles',
                                url:'#'
                            },

                        ],
            dc:         [
                            {
                                voce: 'Terms Of Use',
                                url:'#'
                            },
                            {
                                voce: 'Privacy policy (New)',
                                url:'#'
                            },
                            {
                                voce: 'Ad Choices',
                                url:'#'
                            },
                            {
                                voce: 'Advertising',
                                url:'#'
                            },
                            {
                                voce: 'Jobs',
                                url:'#'
                            },
                            {
                                voce: 'Subscriptions',
                                url:'#'
                            },
                            {
                                voce: 'Talent Workshops',
                                url:'#'
                            },
                            {
                                voce: 'CPSC Certificates',
                                url:'#'
                            },
                            {
                                voce: 'Ratings',
                                url:'#'
                            },
                            {
                                voce: 'Shop Help',
                                url:'#'
                            },
                            {
                                voce: 'Contact Us',
                                url:'#'
                            },
                        ],
            
            sites:      [
                            {
                                voce: 'DC',
                                url:'#'
                            },
                            {
                                voce: 'MAD Magazine',
                                url:'#'
                            },
                            {
                                voce: 'DC Kids',
                                url:'#'
                            },
                            {
                                voce: 'DC Universe',
                                url:'#'
                            },
                            {
                                voce: 'DC Power Visa',
                                url:'#'
                            },
                            

                        ],
            
            social:     [
                            {
                                url: require ('../assets/footer-facebook.png') ,
                                nome: 'facebook'
                            },
                            {
                                url: require ('../assets/footer-twitter.png'),
                                nome: 'twitter'
                            },
                            {
                                url: require ('../assets/footer-youtube.png'),
                                nome: 'youtube'
                            },
                            {
                                url: require ('../assets/footer-pinterest.png'),
                                nome: 'pinterest'
                            },
                            {
                                url: require ('../assets/footer-periscope.png'),
                                nome: 'periscope'
                            },

                        ]
        }
    }
}
</script>

<style lang="scss">
    @import '../styles/variabili_colore.scss';

    footer{
        height: calc(100% - 250px);
        background-image: url('../assets/footer-bg.jpg');
        background-repeat: no-repeat;
        background-size: cover;

        .wrapper-top{
            height: 130px;
            background-color: $backgrund_footer_top;
            ul{
                display: flex;
                align-items: center;
                justify-content: space-between;
                height: 100%;
                padding: 10px;

                li{
                    list-style: none;
                    
                    .wrapper-link{
                            display: flex;
                            align-items: center;
                            justify-content: center;

                        .img_link{
                            width: 40px;
                            margin-right: 10px;
                            
                            img{
                                max-width: 100%;
                                object-fit: cover;
                                                             
                            }
                        }

                        a{
                            line-height: 100%;
                            text-decoration: none;
                            color: $color_text;
                        }
                    }
                }
            }

        }

        .wrapper-mid{
            height: calc(100% - 230px);

            .cols{
                display: flex;
                justify-content: space-between;
                height: 100%;

                .col{
                    width: 50%;
                    height: 100%;
                    display: flex;
                    padding-top: 50px;
                }

                .col-img{
                    width: 50%;

                    img{
                        width: 100%;
                        height: 100%;
                        object-fit: cover;
                    }
                }
            }
        }

        .wrapper-bot{
            height: 100px;
            background-color: $backgrund_footer_bot;


            .wrapper-footer-bot{
                height: 100%;
                display: flex;
                justify-content: space-between;
                align-items: center;

                .btn{
                    padding: 10px;
                    font-size: 18px;
                    border: 1px solid #0282f9;
                    color: white;
                    background-color: $backgrund_footer_bot;
                }

                .social{
                    display: flex;
                    align-items: center;
                    color: #0282f9;

                    img{
                        margin-left: 15px;
                    }
                }
            }
        }
    }

</style>