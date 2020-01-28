<template>
  <div class="grid-part">
    <h1 class="title">display: grid;</h1>

    <section class="container">
      <section class="main">
        <section class="align-items blue">
          <h2>align-items:</h2>
          <img class="justify-center" src="~/assets/grid-ver.png" alt="Grid vertical positions" />
          <h2>align-self</h2>
        </section>

        <section class="justify-items green">
          <h2 class="justify-all">justify-items:</h2>
          <img src="~/assets/grid-hor.png" alt="Grid horizontal positions" />
          <h2 class="justify-self">justify-self</h2>
        </section>
      </section>

      <section class="additional">
        <p>grid-template-(rows/columns): 1fr, 2fr...;(fr,px,%,auto)</p>
        <p>grid-template-areas:</p>
        <p class="grid-template-areas red">"head head head</p>
        <p class="grid-template-areas green">
          <span class="blue">nav</span> main main
        </p>
        <p class="grid-template-areas green">
          <span class="blue">nav</span> main main"
        </p>
        <p>
          grid-area:
          <span class="red">head</span>/
          <span class="blue">nav</span>/
          <span class="green">main</span>;
        </p>

        <hr />

        <div class="grid">
          <div>
            <p class="blue">
              1.) align-items/content:
              start;
            </p>
            <p class="green">
              2.) justify-items/content:
              center;
            </p>
          </div>
          <p>
            = place-items/c:
            <span class="blue">(1.align-items/c)</span>
            <span class="green">(2.justify-items/c)</span>;
          </p>
        </div>
      </section>
    </section>
  </div>
</template>

<script>
export default {}
</script>

<style lang="css" scoped>
p {
  font-size: 1.2em;
}

.container {
  display: flex;
  justify-content: space-around;
}

.align-items,
.justify-items {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  align-items: center;
}

.additional {
  display: flex;
  flex-direction: column;
}

.justify-all::after,
.justify-self::after {
  position: relative;
  right: 50%;
  top: 25px;
  color: var(--red);
}

.justify-all::after {
  content: 'ALL';
}
.justify-self::after {
  content: 'ONE';
}

.justify-center {
  justify-self: center;
  position: relative;
}

.grid-template-areas {
  position: relative;
  padding-left: 5vw;
}
.grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  align-items: center;
  font-size: 0.7em;
}
</style>