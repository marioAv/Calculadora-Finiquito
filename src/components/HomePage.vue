<template>
  <v-content>
  <div class="title">
  <h2>Calcula tu Finiquito</h2>
  <p>Esta calculadora es solamente para fines informativos </p>
  </div>
  <AppForm/>
  <PriceBox/>
  </v-content>
</template>

<script>
import PriceBox from './PriceBox.vue'
import AppForm from './AppForm.vue'

export default {
    components:{
      AppForm,
      PriceBox
    },
  data(){
    return{
      title:"Home Component"
}
}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../assets/common-styles.scss';
body{
  margin:0;
  padding:0;
  background-color:#F7FAFD;
}
.price-box{
    background-color:white;
    padding:25px 45px;
    margin-top:50px;
    border:2px solid white;
    border-radius:8px;
    height:400px;
    width:500px;
    box-shadow: 0px 10px 10px #E1EBF8;
    width:40%;
    float:left;
}
.app-form-container{
  width:50%;
  float:left;
  padding:20px;
}
.title{
  padding:80px 0px 20px 80px;
}
h2,h4{
  font-family:$secondaryFont;
}
p{
  font-family:$secondaryFont;
}
</style>
