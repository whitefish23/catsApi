<template>
  <div class="container">
    <div class="check-wrap">
    <input type="checkbox" v-model="formParams.hasBreed" /> One Breed?
    </div>
    <div>
    <select v-model="formParams.selectedBreeds">
      <option v-for="breed in breedsOptions" :value="breed.id">{{ breed.label }} </option>
    </select>
    <div class="choos-select">Сhoose a breed</div>
    </div>
  </div>
</template>

<script>
import CatCard from '@/components/CatCard.vue';

export default {
  name: 'FilterPage',

  components: {
    CatCard
  },

  created() {
    this.getBreeds()
  },

  data: () => ({
    formParams: {
      selectedBreeds: null,
      hasBreed: false
    },

    breeds: [],
    selectedBreeds: null
  }),



  computed: {
    breedsOptions() {
      return this.breeds.map(i => ({
        id: i.id,
        label: i.name
      }))
    }
  },

  methods: {
    async getBreeds() {
      try {
        const responce = await fetch(`https://api.thecatapi.com/v1/breeds`, {
          headers: {
            'x-api-key': "live_ujFtmrCOJEKcDvtFPkMzjZYNuXoj4ZUiX1FkhFrQFgWnG5E81EaGKpy75rhUwH6r",
          },
        })

        const breeds = await responce.json()

        this.breeds = breeds
      } catch (e) {

      }
    },
  },

  watch: {
    formParams: {
      handler(value) {
        this.$emit('recalc', {...value})
      },
      deep: true,
    }
  }
}
</script>

<style lang="scss">
.check-wrap {
  margin-bottom: 20px;
}

.choos-select {
  margin-top: 5px;
}
</style>