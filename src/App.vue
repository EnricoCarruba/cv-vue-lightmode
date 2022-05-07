<template>
  <new-header/>
  <current-stack/>
  <my-portfolio/>
</template>

<script>
import newHeader from "./components/newHeader.vue";
import currentStack from "./components/currentStack.vue";
import myPortfolio from "./components/myPortfolio.vue";

export default {
  name: 'App',
  components: {
    newHeader, currentStack, myPortfolio,
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Sora:wght@100;200;300;400;500;600;700;800&display=swap');
html, body {
  box-sizing: border-box;
  font-family: 'Sora';
  margin: 0;
  padding: 0;
}

</style>
