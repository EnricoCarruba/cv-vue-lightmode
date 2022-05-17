<template>
 
  <new-header/>
  <current-stack/>
  <my-portfolio/>
  <cv-data/>
  <my-education/>
</template>

<script>
import newHeader from "./components/newHeader.vue";
import currentStack from "./components/currentStack.vue";
import myPortfolio from "./components/myPortfolio.vue";
import myEducation from "./components/myEducation.vue"
import CvData from "./components/cvData.vue";




export default {
  name: 'App',
  components: {
    newHeader,
    currentStack,
    myPortfolio,
    myEducation,
    CvData,
    

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
