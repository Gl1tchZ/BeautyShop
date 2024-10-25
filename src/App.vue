<template>
  <HeaderPage/>
  <HomePage/>
</template>

<script>
import HeaderPage from './components/HeaderPage.vue';
import HomePage from './components/HomePage.vue'

export default {
  name: 'App',
  components: {
    HeaderPage,
    HomePage,
  }
}
</script>

<style>
body{margin: 0;padding: 0;box-sizing: border-box;max-width: 100%;}
h1, h2, h3, h4, h5, h6, ul, ol, li, p{margin: 0;padding: 0;}
ul, ol{list-style: none;}
a{text-decoration: none;color: black;}     
img {max-width: 100%;display: block;}
#app {
  font-family: Roboto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  overflow-x: hidden;
}
* {
  box-sizing: border-box;
  user-select: none;
  -webkit-user-select: none;
  -moz-user-select: none;
}
</style>
