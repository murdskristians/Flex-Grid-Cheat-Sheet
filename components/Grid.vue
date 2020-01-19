<template>
  <div>
    <h1 class="grid-title">display: grid;</h1>

    <section class="main">
      <section class="ai">
        <h2>Ai</h2>
        <h2>align-items: y-axis</h2>
        <img src="~/assets/grid-ver.png" alt="Grid vertical positions" />
        <h2>align-self</h2>
      </section>

      <section class="jc">
        <h2>Jc</h2>
        <h2>justify-items: x-axis</h2>
        <img src="~/assets/grid-hor.png" alt="Grid horizontal positions" />
        <h2>justify-self</h2>
      </section>
    </section>

    <section class="additional">
      <p>grid-template-(rows/columns): 1fr, 2fr...;(fr,px,%,auto)</p>
      <p>
        grid-template-areas: "head head head
        nav main main
        nav main main"
      </p>
      <p>grid-area: head/nav/main;</p>
      <p>
        align-items: start;
        justify-items: center;
      </p>
      <p>place-items: start center;</p>
    </section>

    <h3>ALL</h3>
    <h3>ONLY ONE</h3>
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

.ai,
.jc {
  display: flex;
  place-items: center;
  place-content: space-around;
}

.additional {
  display: flex;
  flex-direction: column;
}
</style>