<template>
  <new-header/>
  <current-stack/>
  <my-portfolio/>
  <my-cv/>
  <my-education/>
</template>

<script>
import newHeader from "./components/newHeader.vue";
import currentStack from "./components/currentStack.vue";
import myPortfolio from "./components/myPortfolio.vue";
import myCv from "./components/myCv.vue";
import myEducation from "./components/myEducation.vue"


export default {
  name: 'App',
  components: {
    newHeader, currentStack, myPortfolio, myCv, myEducation,
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

/* button {
  height: 3rem;
  padding: 0.2rem;
  border-radius: 1.5rem;
  background: linear-gradient(-45deg, #9925ea, #338aff, #9925ea);
  background-size: 400%;
  background-position: 90% 0;
  color: #ffffff;
  transition: background 0.8s;
}

button:hover {
  background-position: 185% 50%;
} */

button {
  height: 5vh;
  width: 30vw;
  background-color: lightsalmon;
  color: white;
  border: none;
  cursor: pointer;
}

button:hover{
  background-color: salmon;
}

</style>
