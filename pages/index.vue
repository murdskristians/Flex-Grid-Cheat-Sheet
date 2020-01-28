<template>
  <div class="container">
    <div>
      <grid />
      <hr class="split" />
      <flex />
    </div>
  </div>
</template>

<script>
import Grid from '~/components/Grid.vue'
import Flex from '~/components/Flex.vue'

export default {
  components: {
    Grid,
    Flex
  }
}
</script>

<style>
:root {
  --red: #c48181;
}

@media screen and (max-width: 900px) {
  .main .align-items,
  .main .justify-items {
    /* grid-template-columns: 1fr; */
    padding-bottom: 20px;
  }
  * {
    justify-items: center;
  }
  .title {
    font-size: 1.7em;
    padding-bottom: 40px;
  }
  h2 {
    font-size: 0.9em;
  }
  .flex-part p,
  .grid-part p {
    font-size: 0.7em;
    padding: 20px 20px 0 20px;
  }
  .grid-part .container {
    flex-direction: column;
  }
  .flex-part div.container {
    display: grid;
    grid-template-columns: 1fr;
  }
  .grid-part .justify-items,
  .flex-part .justify-items {
    grid-template-areas:
      'pic pic pic pic pic'
      'all all . self self';
  }
  .flex-part .main {
    width: 100%;
  }
  .flex-part .main .justify-items {
    display: grid;
  }
  .grid-part .justify-items img,
  .flex-part .justify-items img {
    grid-area: pic;
    padding-bottom: 20px;
    width: 60vw;
  }
  .grid-part .justify-items .justify-all,
  .flex-part .justify-items .justify-all {
    grid-area: all;
  }
  .grid-part .justify-items .justify-self,
  .flex-part .justify-items .justify-self {
    grid-area: self;
  }
  .flex-part .align-items img {
    margin-bottom: 10px;
  }
}
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  background-color: #fffdf9;
}

body {
  font-family: 'Roboto', sans-serif;
}
.title {
  position: relative;
  text-align: center;
  margin: 2vh 0 2vh 0;
  font-weight: bold;
  color: #7e6551;
}
.split {
  margin: 10px 0 5px 0;
  height: 4px;
  background: black;
}
.blue {
  color: #7470d1;
}
.green {
  color: #7cc19c;
}
.red {
  color: var(--red);
}
.red-circle {
  border: var(--red);
  border-style: solid;
  padding: 5px;
  border-radius: 50%;
}
.darkmode--activated .title,
p,
span {
  background-color: transparent;
}
.darkmode--activated img {
  background-color: transparent;
  filter: invert(1);
}
</style>
