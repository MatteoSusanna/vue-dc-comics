<template>
  <div id="app">
    

    <MyHeader />
    <MyJumbo />
    <MyMain />
    <MyFooter />

  </div>
</template>

<script>
import MyHeader from './components/MyHeader'
import MyJumbo from './components/MyJumbo'
import MyMain from './components/MyMain'
import MyFooter from './components/MyFooter'

export default {
  name: 'App',
  components: {
    MyHeader,
    MyJumbo,
    MyMain,
    MyFooter

  }
}
</script>

<style lang="scss">

  @import './styles/variabili_colore.scss';
  @import './styles/generali.scss';

  html{
    font-family: sans-serif;
  }
</style>
