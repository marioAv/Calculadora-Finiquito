<template>
  <v-app>
    <v-content>
     <AppHeader/>
     <HomePage/>
    </v-content>
  </v-app>
</template>

<script>
import AppHeader from './components/AppHeader.vue'
import HomePage from './components/HomePage.vue'

export default {
  name: 'App',
  components: {
    AppHeader,
    HomePage
  },
  data () {
    return {
      //
    }
  }
}
</script>
<style lang="scss">
@import 'assets/common-styles.scss';

</style>