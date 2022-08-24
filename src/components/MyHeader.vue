<template>
    <header>
        <div class="container">
            <div class="logo">
                <img src="@/assets/dc-logo.png" alt="">
            </div>
            <nav>
                <ul>
                    <li v-for="(link, indice) in links" :key="indice">
                        <a :href="link.direzione">{{link.nome}}</a>
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<script>
export default {
    nome: 'MyHeader',
    data(){
        return{
            links:  [
                        {
                            'nome': 'CHARACTERS',
                            'direzione': '#',
                            'attivo': false
                        },
                        {
                            'nome': 'CIMICS',
                            'direzione': '#',
                            'attivo': true
                        },
                        {
                            'nome': 'MOVIES',
                            'direzione': '#',
                            'attivo': false
                        },
                        {
                            'nome': 'TV',
                            'direzione': '#',
                            'attivo': false
                        },
                        {
                            'nome': 'GAMES',
                            'direzione': '#',
                            'attivo': false
                        },
                        {
                            'nome': 'COLLECTIBLES',
                            'direzione': '#',
                            'attivo': false
                        },
                        {
                            'nome': 'VIDEOS',
                            'direzione': '#',
                            'attivo': false
                        },
                        {
                            'nome': 'FANS',
                            'direzione': '#',
                            'attivo': false
                        },
                        {
                            'nome': 'NEWS',
                            'direzione': '#',
                            'attivo': false
                        },
                        {
                            'nome': 'SHOP',
                            'direzione': '#',
                            'attivo': false
                        },

                    ]
        }
    }
}
</script>

<style lang="scss">
    @import '../styles/variabili_colore.scss';
    header{
        height: 150px;
        padding-top: 10px;

        .logo{
            display: flex;
            align-items: center;
        }

        .container{
            display: flex;
            justify-content: space-between;
            align-content: center;
                
            ul{
                display: flex;
                align-content: center;
                list-style: none;
                height: 100%;

                li{
                    display: flex;
                    align-items: center;
                    justify-content: center;
                    a{
                        text-decoration: none;
                        color: $color_text_nav;
                        font-weight: bold;
                        margin: 0 10px;
                    }
                }

            }
                


        }
    }


</style>
