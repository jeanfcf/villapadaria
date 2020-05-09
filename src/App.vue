<template>
  <div id="app">
      <c-navbar/>
      <c-home/>
  </div>
</template>

<script>
import cNavbar from './components/navbar/Navbar.vue';
import cHome from './components/Home.vue';
export default {
  name: 'App',
  components: {
    cHome,
    cNavbar
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