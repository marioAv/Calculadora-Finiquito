<template>
  <div class="hello">
    <header>
        <img class="app-logo" v-bind:src="logo">
        <img class="hamb-menu" v-bind:src="hamburguerMenu">
      </header>
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
    logo:"https://www.underconsideration.com/brandnew/archives/bank_of_america_logo_stacked_a.png",
    hamburguerMenu:"https://static.thenounproject.com/png/217838-200.png",
    dailyPayment:" ",
    name:"mario",
    months:['Enero', 'Febrero', 'Marzo', 'Abril', 'Mayo', 'Junio', 'Julio', 'Agosto', 'Septiembre', 'Octubre','Noviembre', 'Diciembre'],
    days:[1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21]
    }
}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
$logoWidth:150px;


.app-logo{
  width:$logoWidth;
}
.hamb-menu{
  width: 50px;
}
</style>
