<template>
<div class="price-box">
<h1>Your Total Payment will be</h1>
<p class="total-payment"><span>$</span> 20000</p>

<div class="breakdown">
<p>Vacaciones</p>
<span>$1000</span>
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

.price-box{
    background-color:white;
    padding:45px;
}

.total-payment{
    color:#004FCA;
    font-weight:bold;
    font-size:50px;
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
    border:2px solid gainsboro;
    border-radius:6px;
    height:400px;
    width:500px;

    button{
        clear:both;
        background-color:red;
    }
}
.breakdown{
    width:20%;
    float:left;
}
</style>