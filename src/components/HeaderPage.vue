<template>
  <div class="container">
  <div class="header">
    <div class="header__title">Cat Home</div>
    <img src="https://w7.pngwing.com/pngs/283/571/png-transparent-whiskers-dog-cat-butterfly-cute-cat-head-mammal-animals-cat-like-mammal.png" alt="" class="header__img">
  </div>
  </div>
</template>
  
<script>
 export default {
    name: 'Header',
  }

</script>
  
<style lang="scss">
.header {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 50px 0px 50px 0px;

  &__title {
    font-size: 22px;
    margin-bottom: 20px;
  }

  &__img {
    width: 15%;
  }
}
</style>