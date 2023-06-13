<template>
  <div class="container">
  <div class="footer">
    <img src="https://assets.karyakarsa.com/header-6231988d5aa7b.jpg" alt="" class="footer__img">
    <div class="footer__title">Cat end</div>
  </div>
</div></template>
  
<script>
export default {
  name: 'footer',
}

</script>
  
<style lang="scss">
.footer {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 50px 0px 50px 0px;

  &__img {
    width: 100%;
    height: 70px;
    object-fit: cover;
  }

  &__title {
    font-size: 22px;
    margin-top: 20px;
  }
}
</style>