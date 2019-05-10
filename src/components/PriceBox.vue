<template>
<div class="price-box">
<h1>Tu pago total sera</h1>
<p class="total-payment"><span>$</span>20000</p>

<div class="breakdown">
<p>Vacaciones</p>
<span>{{vacationDays}}</span>
</div>

<div class="breakdown">
<p>Aguinaldo</p>
<span>$1000</span>
</div>

<div class="breakdown">
<p>Prima Vacacional</p>
<span>$1000</span>
</div>

<div class="breakdown">
<p>Sueldos Pendientes</p>
<span>$1000</span>
</div>

<div class="breakdown">
<p>Otros</p>
<span>$1000</span>
</div>

<button>Calcular Finiquito</button>

</div>

</template>

<script>
export default{
    data(){
        return{
            title:"Price Box should go here"
        }
    }
}
</script>


<style lang="scss">
@import '../assets/common-styles.scss';

.total-payment{
    color:#004FCA;
    font-weight:bold;
    font-size:50px;
    margin:15px 0px;
        span{
            font-size:20px;
        }
}

h1{
    font-family:$primaryFont;
}
p{
    font-family:$primaryFont;
}
span{
    font-family:$secondaryFont;
    font-weight:bold;
}

.price-box{
    button{
        clear:both;
        background-color:#F80021;
        border-radius:6px;
        color:#FEE2E6;
        padding:10px 30px;
        border:0px;
        //  box-shadow: 0px 10px 70px #F80021;
         margin-top:102px;
    }
}
.breakdown{
    width:32%;
    float:left;
}
</style>