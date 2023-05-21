<template>
 <h3>Div {{name}}</h3>
</template>
<script>
export default{
  data:function()
  { 
    return {
      // name:"HomeComponent",
      email:"sahillmandal.786@gmail.com",
    }  
  },
  // props:{
  //   name:string,
  // }
};
   
</script>
<style scoped>
h3{
  width:100px;
  height:100px;
  background-color:black;
  color:orange;
  display:inline-block;
  margin-right: 3px;
  border-radius: 20px;
  padding:10px;
  flex-wrap: wrap;
}
h3:hover{
  border-color: blue;
  border-style: solid;
  border-width: 4px;
}
</style>