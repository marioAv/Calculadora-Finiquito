<template>
        <header>
        <img class="app-logo" v-bind:src="logo">
        <img class="hamb-menu" v-bind:src="hamburguerMenu">
      </header>
</template>

<script>
export default {
    data(){
        return {
            title:"This is the header",
            logo:"https://www.underconsideration.com/brandnew/archives/bank_of_america_logo_stacked_a.png",
            hamburguerMenu:"https://static.thenounproject.com/png/217838-200.png",
        }
    }
}
</script>

<style scoped lang="scss">
$logoWidth:100px;

*{
    margin:0px;
    padding:0px;
}

header{
  border: 1px #E8F0F9;
  box-shadow: 0px 15px #EAF1FA;
  padding:10px;
  background-color:white;
}
.app-logo{
  width:$logoWidth;
}
.hamb-menu{
  width: 50px;
}
</style>