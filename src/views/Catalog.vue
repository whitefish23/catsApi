<template>
  <div class="container">
    <cat-card
      v-for="cat in cats"
      :key="cat.id"
      :src="cat.url"
      :width="cat.width"
      :height="cat.height"
    />
    
  </div>
</template>
  
  
<script lang="js">

import CatCard from '@/components/CatCard.vue';
  
 export default {
   name: 'catalog',

   components: {
     CatCard
   },

   data: () => ({
     cats: [
     {"id":"6m4","url":"https://cdn2.thecatapi.com/images/6m4.jpg","width":540,"height":720},
     {"id":"aov","url":"https://cdn2.thecatapi.com/images/aov.jpg","width":460,"height":500},
     {"id":"bb8","url":"https://cdn2.thecatapi.com/images/bb8.jpg","width":500,"height":335},
     {"id":"cb2","url":"https://cdn2.thecatapi.com/images/cb2.jpg","width":500,"height":316},
     {"id":"d7s","url":"https://cdn2.thecatapi.com/images/d7s.jpg","width":324,"height":394},
     {"id":"dfn","url":"https://cdn2.thecatapi.com/images/dfn.jpg","width":450,"height":569},
     {"id":"Q6TDnfM_O","url":"https://cdn2.thecatapi.com/images/Q6TDnfM_O.jpg","width":1600,"height":1000},
     {"id":"8Ggv2cWP_","url":"https://cdn2.thecatapi.com/images/8Ggv2cWP_.jpg","width":1185,"height":1776},
     {"id":"5Esmfiggi","url":"https://cdn2.thecatapi.com/images/5Esmfiggi.jpg","width":750,"height":561},
     {"id":"HW1MGAuGL","url":"https://cdn2.thecatapi.com/images/HW1MGAuGL.jpg","width":1600,"height":1200}]
   }),
   
   
 }
</script>

<style lang="scss" scoped>
</style>