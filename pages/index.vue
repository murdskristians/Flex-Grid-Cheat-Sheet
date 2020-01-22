<template>
  <div class="container">
    <div>
      <grid />
      <hr class="split">
      <flex />
    </div>
  </div>
</template>


<script>
import Grid from '~/components/Grid.vue'
import Flex from '~/components/Flex.vue'

export default {
  // head () {
  //   return {
  //     script: [
  //       { src: '@/assets/darkmode.js' }
  //     ]
  //   }
  // },
  components: {
    Grid,
    Flex
  }
}

</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Volkhov&display=swap');
@import url('https://fonts.googleapis.com/css?family=Salsa&display=swap');

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  font-family: 'Salsa', cursive;
  background-color: #FFFDF9;
}
.title {
  position: relative;
  text-align: center;
  margin: 2vh 0 2vh 0;
  font-family: 'Volkhov', serif;
  font-weight: bold;
  color: #7E6551;
}
.split {
  margin: 10px 0 5px 0;
}

.blue {
    color: #7470D1;
}
.green {
    color: #7CC19C;
}
.red {
    color: #C48181;
}

.darkmode--activated .title, p, span {
  background-color: transparent;
}

.darkmode--activated img {
  background-color: transparent;
  filter: invert(1);
}
</style>
