<template>
<div class="app-form">
      <h2>Calcula tu Finiquito</h2>
      <p>Esta calculadora es solamente para fines informativos <p>
      <h4>Salary Per Day is ${{dailyPayment}}</h4>
      <p></p>
      <input type="range" name="salary"
             min="170" max="5000" v-model="dailyPayment">

      <h4>Fecha De Ingreso A tu empleo</h4>
      <select class="" name="">
        <option value="">25</option>
      </select>
      <select class="" name="month">
        <option v-for="month in months">{{month}}</option>
      </select>
      <select>
        <option value="">2018</option>
      </select>

      <h4>Fecha De Baja en tu empleo</h4>
      <select class="" name="">
        <option value="">25</option>
      </select>
      <select class="" name="month">
        <option v-for="month in months">{{month}}</option>
      </select>
      <select>
        <option value="">2018</option>
      </select>

      <h4>Te adeudan vacaciones?</h4>
      <button type="button">SI</button>
      <button type="button" name="button">NO</button>

      <h4>Dias de aguinaldo</h4>
      <select>
        <option value="">10</option>
      </select>


      <div>
        <h3>Tu pago total</h3>
        <p>$15000</p>
      </div>
      <button>Calcular</button>
  </div>
</template>

<script>
export default {
    data(){    
      return{
      title:"Form Component"
    }
}
}
</script>

<style lang="scss">
@import '../assets/common-styles.scss';

h2,h4{
  font-family:$primaryFont;
}
p{
  font-family:$secondaryFont;
}
</style>