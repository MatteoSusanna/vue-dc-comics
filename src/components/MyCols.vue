<template>
    <div>
       <div class="cont-col">
            <h2>{{titolo}}</h2>
            <ul>
                <li v-for="(voce, indice) in urls" :key="indice">
                    <a :href="voce.url">{{voce.voce}}</a>
                </li>
            </ul>
       </div>
    </div>
  
</template>

<script>
export default {
    nome: 'MyCols',
    props:{
        titolo: String,
        urls: Object,
    }

}
</script>

<style lang="scss">
    @import '../styles/variabili_colore.scss';
    .cont-col{
        margin-right: 40px;
        height: 100%;

        h2{
            color: $color_text;
            margin: 10px 0;
        }
    
        li{
            list-style: none;
            font-size: 17px;
            color: $color_text_footer;
            line-height: 25px;
                a{
                    text-decoration: none;
                    color: $color_text_footer;
                    &:hover{
                        color: $color_text;
                    }

                }
            }
        }

</style>