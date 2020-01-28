<template>
  <div class="flex-part">
    <h1 class="title">display: flex;</h1>

    <div class="container">
      <div class="main">
        <section class="align-items blue">
          <h2>align-<span class="red-circle">items</span>/ content </h2>
          <img src="@/assets/grid-ver.png" alt="Picture for grid vertical positioning." />
          <h2>align-self</h2>
        </section>

        <section class="justify-items green">
          <h2 class="justify-all">justify-items/<span class="red-circle">content</span></h2>
          <img src="@/assets/flex-hor.png" alt="Picture for grid horizontal positioning." />
          <h2 class="justify-self">justify-self</h2>
        </section>

        <p class="justify-items red">If flex dirrection is column - switch pictures.</p>
      </div>

      <section class="additional">
        <section class="shorthand-flex">
          <p class="blue">1.) flex-grow:1 (take all space)</p>
          <p
            class="red"
          >2.) flex-shrink: 0 (item will be smallest) / 1 (all equal) / 2 (will stay as largest item)</p>
          <p class="green">3.) flex-basis: auto (same as all) / 0 (small as possible / 10px</p>
          <hr />
          <p>
            = flex:
            <span class="blue">(1.grow)</span>
            <span class="red">(2.shrink)</span>
            <span class="green">(3.basis)</span>
          </p>
          <hr />
        </section>

        <section class="shorthand-flexflow">
          <p class="blue">1.) flex-dirrection: row / column</p>
          <p class="green">2.) flex-wrap: no-wrap / wrap</p>
          <hr />
          <p>
            = flex-flow:
            <span class="blue">(1.flex-dirrection)</span>
            <span class="green">(2.flex-wrap)</span>
          </p>
          <hr />
        </section>

        <p>order: 0 (default)</p>
      </section>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="css" scoped>
.container {
  display: grid;
  grid-template-columns: 1fr 1fr;
}

.align-items,
.justify-items {
  display: flex;
  align-items: center;
  justify-content: space-around;
}

.shorthand-flexflow,
.shorthand-flex {
  padding-bottom: 10px;
}
</style>