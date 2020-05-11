<template>
  <div id="app">
      <c-navbar/>
      <c-home/>
      <c-sobre/>
      <c-onde/>
  </div>
</template>

<script>
import cNavbar from './components/navbar/Navbar.vue';
import cHome from './components/home/Home.vue';
import cSobre from './components/sobre/Sobre.vue';
import cOnde from './components/Onde.vue';
export default {
  name: 'App',
  components: {
    cHome,
    cNavbar,
    cSobre,
    cOnde
  }, 
  }

</script>

<style>
  *{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Montserrat';
  }  
</style>