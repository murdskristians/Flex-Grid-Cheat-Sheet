<template>
  <div class="container">
    <div>
      <grid />
    </div>
  </div>
</template>

<script>
import Grid from '~/components/Grid.vue'

export default {
  components: {
    Grid
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
}
</style>
