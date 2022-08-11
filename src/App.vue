<template>
    <pokeVue :pokemons="pokemons"/>
</template>

<script>
import pokeVue from './components/poke.vue';

export default {
  name: "App",
  components: {
    pokeVue
  },
  
  data() {
    return{
      pokemons:[]
    }
  }

}
</script>

<style>

</style>