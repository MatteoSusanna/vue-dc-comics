<template>
    <div class="comic">
        <div class="comics-img">
            <img :src="fumetti.thumb" alt="">
        </div>
        <h4>{{fumetti.series}}</h4>
    </div>
</template>

<script>
export default {
    nome: 'CardComics',
    props:  {
                fumetti: Object,
            }
}
</script>

<style lang="scss">

    .comics{
                display: flex;
                justify-content: space-between;
                align-items: center;
                flex-wrap: wrap;
                .comic{
                    width: calc(100% / 6 - 1rem);
                    .comics-img{
                        width: 100%;
                        height: 200px;
                        img{
                            width: 100%;
                            height: 100%;
                            background-size: contain;
                            
                        }
                    }
                }
            }

</style>