<template>
    <div class="container">
        <div class="bloco-1">
           <ul>
                <li v-for="item in pokemons" :key="item.name">
                    {{item.name}}
                </li>
           </ul>
        </div>
          <div class="bloco-2">
            pokemons
        </div>
      
    </div>
    
</template>

<script>
export default {
    name: "poke",
    props: {
        pokemons:[]
    },

    data() {
    return{
      pokemon: null
    }
  },
    
}
</script>

<style>
    .container {
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
    }

    .bloco-1 {
        border: 2px solid black;
        order: 0;
        flex-grow: 0;
    }

    .bloco-2 {
        border: 2px solid black;
        order: 0;
        flex-grow: 0;
    }
</style>