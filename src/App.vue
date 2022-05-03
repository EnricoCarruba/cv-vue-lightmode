<template>
  <main-header/>
</template>

<script>
import MainHeader from "./components/MainHeader.vue";

export default {
  name: 'App',
  components: {
    MainHeader,
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Sora:wght@100;200;300;400;500;600;700;800&display=swap');

#app {
  
  font-family: 'Sora';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 30px;
}
</style>
