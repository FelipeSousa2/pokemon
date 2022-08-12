<template>
    <header>
        <h1>Catálogo</h1>
        <h2>pokemons</h2>
    </header>
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



<style lang="less" scoped>

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