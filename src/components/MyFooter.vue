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
                            <div class="cont-col">
                                <h2>DC COMICS</h2>
                                <ul>
                                    <li>Comics</li>
                                    <li>Movies</li>
                                    <li>TV</li>
                                    <li>Comics</li>
                                    <li>Movies</li>
                                    <li>TV</li>
                                    <li>Comics</li>
                                </ul>

                                <h2>SHOP</h2>
                                <ul>
                                    <li>Shop DC</li>
                                    <li>ShopDC Collectibles</li>
                                </ul>
                            </div>

                            <div class="cont-col">
                                <h2>DC</h2>
                                <ul>
                                    <li>Comics</li>
                                    <li>Movies</li>
                                    <li>TV</li>
                                    <li>Comics</li>
                                    <li>Movies</li>
                                    <li>TV</li>
                                    <li>Comics</li>
                                    <li>Comics</li>
                                    <li>Movies</li>
                                    <li>TV</li>
                                    <li>Comics</li>
                                </ul>
                            </div>

                            <div class="cont-col">
                                <h2>SITES</h2>
                                <ul>
                                    <li>Comics</li>
                                    <li>Movies</li>
                                    <li>TV</li>
                                    <li>Comics</li>
                                    <li>Movies</li>
                                </ul>
                            </div>

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
export default {
    nome: 'MyFooter',
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
                                width: 100%;
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
            overflow-y: hidden;

            .cols{
                display: flex;
                justify-content: space-between;

                .col{
                    width: 50%;
                    display: flex;
                    padding: 50px;

                    .cont-col{
                        margin-right: 40px;

                        h2{
                            color: $color_text;
                            margin: 10px 0;
                        }
    
                        li{
                            list-style: none;
                            font-size: 17px;
                            color: $color_text_footer;
                            line-height: 25px;
                        }
                    }

                }

                .col-img{
                    width: 50%;
                    height: 500px;
                    bottom: 50%;
                    

                    img{
                        width: 100%;
                        height: 100%;
                        object-fit: contain;
                        overflow: hidden;
                        
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