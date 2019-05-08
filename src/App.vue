<template>
  <div id="app">
    <AppHeader/>
    <AppForm/>
    <PriceBox/>
  </div>
</template>

<script>
import HomePage from './components/HomePage.vue'
import PriceBox from './components/PriceBox.vue'
import AppHeader from './components/AppHeader.vue'
import AppForm from './components/AppForm.vue'

export default {
  name: 'app',
  components: {
    HomePage,
    PriceBox,
    AppHeader,
    AppForm
  }
}
</script>

<style lang="scss">
@import 'assets/common-styles.scss';


body{
  margin:0;
  padding:0;
  background-color:#F7FAFD;
}
.app-form{
  width:45%;
  float:left;
}
.price-box{
  width:40%;
  float:left;
}

</style>
