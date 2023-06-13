<template>
  <div class="container">
    <FilterPage @recalc=getCats />
    <div class="row">
        <CatCard :cats="cats"  />
    </div>
  </div>
</template>

<script>
import CatCard from '@/components/CatCard.vue';
import FilterPage from '@/components/FilterPage.vue'
import queryString from 'query-string';

export default {
  name: 'Catalog',

    components: {
      CatCard, FilterPage
    },
  
    created() {
      this.getCats()
    },

    data: () => ({
      cats: [],
    }),

    methods: {
      async getCats({selectedBreeds, hasBreed } = {}) {

        const params = queryString.stringify({
          limit: 14,
          has_breeds: hasBreed,
          order: 'none',
        })

         if(selectedBreeds) {
          params.breed_ids = selectedBreeds
        }


        try {
          const responce = await fetch(`https://api.thecatapi.com/v1/images/search?${queryString.stringify(params)}`, {
            headers: {
              'x-api-key': "live_ujFtmrCOJEKcDvtFPkMzjZYNuXoj4ZUiX1FkhFrQFgWnG5E81EaGKpy75rhUwH6r",
            },
          })

          const cats = await responce.json()

          this.cats = cats
        } catch (e) {
          console.log('Err')
        }
      }
    }
}
</script>

<style lang="scss"></style>