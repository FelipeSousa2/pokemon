<template>
    <pokeVue :pokemons="pokemons"/>
</template>

<script>
import pokeVue from './components/poke.vue';

import{api} from './services/services'

export default {
  name: "App",
  components: {
    pokeVue
  },
  
  data() {
    return{
      pokemons:[]
    }
  },

  created() {
       api.get('pokemon').then(data => this.pokemons = data.data.results)
    }

}
</script>

<style>
  

 
</style>