<template>
  <div id="app">
      <c-navbar/>
      <div class="teste"></div>
      <div id="home"></div>
  </div>
</template>

<script>
import cNavbar from './components/Navbar.vue';
export default {
  name: 'App',
  components: {
    cNavbar
  }, 
  }

</script>

<style>
  *{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Montserrat'
  }  

  .teste{
    height: 200vh;
    background-color: #1A8ACB;
    width: 100%;
  }

  #home{
    height: 200vh;
    background-color: blueviolet;
    width: 100%;
  }
</style>