<template>

 
    <img class="CatCard" v-bind:src='`../views/catalog/${{url}}`'/> 
    
 

  </template>
  
  
  <script lang="js">

  export default {
    name:'CatCard',
    props: {
      id:{
        type:String,
        requared:true
      },
      
      url:{
        type:String,
        requared:true
      },
      width:{
        type:Number,
        requared:true
      },

      height:{
        type:Number,
        requared:true
      },
      
    }
  }
  </script>

<style lang="scss" scoped>
.CatCard {
  width: 100px;
  height: 100px;
  object-fit: cover;
  margin: 5px;
  padding: 10px;
  background: #ecf0f3;
  border-radius: 3px;
  box-shadow: -6px -6px 10px rgba(255, 255, 255, 0.8),
    6px 6px 10px rgba(0, 0, 0, 0.2);
}
</style>