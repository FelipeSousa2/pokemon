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
  template {
        font-family: Arial, Helvetica, sans-serif;
    }

    header > h1 h2 {
        margin: auto;
        
    }

   
    .container {
        border-radius: 10px 10px;
        border: 2px solid white;
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        flex-wrap: wrap;
        row-gap: 10px;
        column-gap: 30px;
        background-color: #f9eac3;
        color: black;
        padding: 16px;
        height: 550px;
        width: 700px;
    }

   

    .bloco-1 {
        box-shadow: 2px 2px rgba(0, 0, 0, 0.562);
        border: 2px solid black;
        order: 0;
        flex: 0 1 auto;
       
    }

    .bloco-2 {
        flex-basis: auto;
        height: 500px;
        width: 400px;
        box-shadow: 2px 2px rgba(0, 0, 0, 0.562);
        border: 2px solid black;
        order: 0;
        flex: 0 1 auto;
    }

 
</style>