<template>
  <div class="cat-card col-xs-12">
    <div class="cat-card__cat-card" v-for="cat in cats">
      <img class="cat-card__img" :src="cat.url" alt="" />
      <div class="cat-card__name"> Name: {{ cat.breeds[0].name }}</div>
      <div class="cat-card__origin"> Origin: {{ cat.breeds[0].origin }}</div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    cats: {
      type: Array,
      required: true,
    }
  }
}
</script>

<style lang="scss" scoped>
.cat-card {
  display: flex;
  flex-wrap: wrap;

  &__cat-card {
    width: 280px;
    height: 265px;
    object-fit: cover;
    margin: 10px;
    padding: 15px;
    background: #ecf0f3;
    border-radius: 3px;
    box-shadow: -6px -6px 10px rgba(255, 255, 255, 0.8),
      6px 6px 10px rgba(0, 0, 0, 0.2);
  }

  &__img {
    width: 100%;
    height: 150px;
    border-radius: 3px;
    object-fit: cover;
  }

  &__name {
    font-size: 14px;
    font-weight: 500;
    margin: 20px 0px 10px;
  }

  &__origin {
    font-size: 14px;
    font-weight: 500;
    
  }

  &__description {
    font-size: 12px;
    margin: 0 10px;
    overflow-wrap: break-word;
    color: silver;
  }
}
</style>