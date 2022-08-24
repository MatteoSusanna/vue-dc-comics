<template>
    <main>
        <div class="container">
            <h2>Content goes here</h2>
        </div>
    </main>
</template>

<script>
export default {
    nome: 'MyMain'
}
</script>

<style lang="scss">
    @import '../styles/variabili_colore.scss';
    main{
        height: 100px;
        background-color: $backgrund_main;
        color: $color_text;
        line-height: 100px;
    }

</style>