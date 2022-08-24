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


</style>
