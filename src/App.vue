<template>
  <div id="app">
    <HomePage/>
    <PriceBox/>
  </div>
</template>

<script>
import HomePage from './components/HomePage.vue'
import PriceBox from './components/PriceBox.vue'

export default {
  name: 'app',
  components: {
    HomePage,
    PriceBox
  }
}
</script>

<style>

</style>
