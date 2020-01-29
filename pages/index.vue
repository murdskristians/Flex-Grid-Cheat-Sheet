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
  body {
    min-width: 340px;
  }
  .main .align-items,
  .main .justify-items {
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
    padding: 0 20px 0 20px;
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
  .additional {
    padding: 40px 20px 10px 20px;
  }
  .darkmode-toggle {
    z-index: 1;
  }
  .justify-all::after,
  .justify-self::after {
    color: var(--red);
    position: relative;
    right: 50%;
    top: 25px;
  }
}
@media screen and (min-width: 500px) and (max-width: 900px) {
  .title {
    font-size: 1.9em;
  }
  h2 {
    font-size: 1.7em;
  }
  .flex-part p,
  .grid-part p {
    font-size: 1em;
  }
  .grid-part .justify-items img,
  .flex-part .justify-items img {
    padding-bottom: 20px;
    width: 30vw;
  }
}
@media screen and (min-width: 900px) and (max-width: 1275px) {
  .justify-all::after,
  .justify-self::after {
    color: var(--red);
    position: relative;
    padding-left: 10px;
    top: 0;
    left: 0;
  }
}
@media screen and (min-width: 1275px) {
  .justify-all::after,
  .justify-self::after {
    color: var(--red);
    position: relative;
    right: 50%;
    top: 25px;
  }
}
/* Not a media querry */
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
.container {
  padding: 20px;
}
.additional {
  padding-left: 20px;
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
  filter: invert(1) contrast(0.15) hue-rotate(300deg);
}
.darkmode--activated p:not(.blue, .red, .green) {
  color: rgb(87, 36, 36);
}
.darkmode-toggle {
  z-index: 1;
}
</style>
