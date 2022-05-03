<template>
  <new-header/>
  <current-stack/>
  <toggle-buttons/>
</template>

<script>
import newHeader from "./components/newHeader.vue";
import currentStack from "./components/currentStack.vue";
import toggleButtons from "./components/toggleButtons.vue";

export default {
  name: 'App',
  components: {
    newHeader, currentStack, toggleButtons,
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
  margin-top: 0px;
}
</style>
