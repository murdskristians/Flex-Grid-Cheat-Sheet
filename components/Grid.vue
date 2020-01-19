<template>
  <div>
    <h1 class="grid-title">display: grid;</h1>

    <section class="container">
      <section class="main">
        <section class="ai blue">
          <h2>align-items:</h2>
          <img class="justify-center" src="~/assets/grid-ver.png" alt="Grid vertical positions" />
          <h2>align-self</h2>
        </section>

        <section class="ji green">
          <h2 class="justify-all">justify-items:</h2>
          <img src="~/assets/grid-hor.png" alt="Grid horizontal positions" />
          <h2 class="justify-self">justify-self</h2>
        </section>
      </section>

      <section class="additional">
        <p>grid-template-(rows/columns): 1fr, 2fr...;(fr,px,%,auto)</p>
        <p>grid-template-areas:</p>
        <p class="grid-template-areas red">"head head head</p>
        <p class="grid-template-areas green"> <span class="blue">nav</span>  main main</p>
        <p class="grid-template-areas green"> <span class="blue">nav</span> main main"</p>
        <p>grid-area: head/nav/main;</p>
        <div class="grid">
          <div>
            <p>align-items: <span class="blue"> start</span>;</p>
            <p>justify-items: <span class="green"> center</span>;</p>
          </div>
          <p>place-items: <span class="blue">start</span> <span class="green"> center</span>;</p>
        </div>
      </section>
    </section>
  </div>
</template>

<script>
export default {}
</script>

<style lang="css" scoped>
.grid-title {
  position: relative;
  text-align: center;
  margin: 2vh 0 2vh 0;
}

p {
 font-size: 1.2em;
}
.container {
  display: flex;
  justify-content: space-around;
}

.ai,
.ji {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  align-items: center;
}

.additional {
  display: flex;
  flex-direction: column;
}

.justify-all::after {
  content: 'ALL';
  position: relative;
  right: 50%;
  top: 25px;
  color: red;
}
.justify-self::after {
  content: 'ONE';
  position: relative;
  right: 50%;
  top: 25px;
  color: red;
}

.justify-center {
  justify-self: center;
  position: relative;
}

.grid-template-areas {
  position: relative;
  left: 10vw;
}
.grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  align-items: center;
}

.blue {
    color: rgb(18, 4, 100)
}
.green {
    color: rgb(15, 97, 0)
}
.red {
    color: rgb(102, 0, 0)
}
</style>