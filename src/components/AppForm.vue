<template>
<v-content class="app-form-container" >
    <div class="app-form">
      <h4>Cual es tu salario diario?</h4>
      <p>${{dailyPayment}}</p>
      <v-slider max="1500" min="200" v-model="dailyPayment"></v-slider>

      <h4>Cuantos dias de aguinaldo tienes por año?</h4>
      <p>{{christmasBonus}} Días</p>
      <v-slider max="60" min="5" v-model="christmasBonus"></v-slider>

      <h4>Fecha de ingreso</h4>
      <v-menu>
        <v-text-field v-bind:value="fechaIngreso" slot="activator" prepend-icon="date_range"></v-text-field>
        <v-date-picker v-model="fechaIngreso" header-color="#004FCA"></v-date-picker>
      </v-menu>

      <h4>Fecha de Baja</h4>
      <v-menu>
        <v-text-field v-bind:value="fechaBaja" slot="activator" prepend-icon="date_range"></v-text-field>
        <v-date-picker v-model="fechaBaja" header-color="#004FCA"></v-date-picker>
      </v-menu>


      <h4>Te adeudan vacaciones?</h4>
      <v-btn type="button" color="#004FCA" dark v-on:click="hasVacations = true"> SI</v-btn>
      <v-btn type="button" color="#004FCA" dark v-on:click="hasVacations = false"> NO</v-btn>

      <div v-if="hasVacations">
      <h4>Cuantos Dias de vacaciones tienes al año?</h4>
      <p>{{vacationTotalDays}} Días</p>
      <v-slider max="35" min="6" v-model="vacationTotalDays"></v-slider>

      <h4>Cual es tu prima vacacional?</h4>
      <p>{{vacationBonus}}%</p>
      <v-slider max="100" min="5" v-model="vacationBonus"></v-slider>
      </div>

      <!--TOTAL VACATION PAYMENT-->
      <!-- <h1>{{vacationTotalDays * dailyPayment}}</h1> -->

      <!--TOTAL CHRISTMAS PAYMENT --> 
      <v-btn type="button" color="#004FCA" dark 
             v-on:click="datenumber" v-if="fechaBaja && fechaIngreso">Calcular Aguinaldo</v-btn>

      <p v-if="diasTrabajados"> ${{ dailyPayment * christmasBonus / 365 * diasTrabajados}}</p>


  </div>
</v-content>
</template>

<script>
export default {
    data(){    
      return{
          title:"Form Component",
          fechaIngreso:null,
          fechaBaja:null,
          dailyPayment:500,
          hasVacations:false,
          vacationTotalDays:10,
          vacationBonus:25,
          christmasBonus:15,

          fechaBajaMseconds:null,
          fechaIngresoMseconds:null,
          diasTrabajados:null,
          }
    },
    methods: {
        datenumber: function getDate(){
        let baja = Date.parse(this.fechaBaja);
        let ingreso = Date.parse(this.fechaIngreso);

        this.fechaBajaMseconds = baja;
        this.fechaIngresoMseconds = ingreso;

        this.diasTrabajados= (baja - ingreso) / (1000 * 60 * 60 * 24);
 }
    },
}

</script>

<style lang="scss" scoped>
@import '../assets/common-styles.scss';

h2,h4{
  font-family:$secondaryFont;
}
p{
  font-family:$secondaryFont;
}
.v-input{
  width:85%;
  margin-top:0px;
}
.v-btn{
  margin:7px 10px 7px 0px;
  margin-top:5px;
  margin-right:10px;
}
.v-menu{
  display: block;
  width:85%;
}
.app-form{
  padding:50px 80px;
      p{
        font-size:25px;
        font-weight: bold;
        margin:0px 0px;
      }
}
</style>