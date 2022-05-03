<template>
  <main-header/>
  <current-stack/>
  <toggle-buttons/>
</template>

<script>
import MainHeader from "./components/MainHeader.vue";
import currentStack from "./components/currentStack.vue";
import toggleButtons from "./components/toggleButtons.vue";

export default {
  name: 'App',
  components: {
    MainHeader, currentStack, toggleButtons,
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
