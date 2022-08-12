<template>
    <header>
        <h1>Catálogo pokemons</h1>
        
    </header>
    <div class="container">
        <div class="bloco-1">
           <button class="btn-group">
               <ul>
                    <li v-for="item in pokemons" :key="item.name">
                        {{item.name}}
                    </li>
               </ul>
           </button>
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

    template {
        font-family: Arial, Helvetica, sans-serif;
    }

    header > h1 {
        margin: auto;
        margin-bottom: 5pt;
    }

   
    .container {
        font-family: Arial, Helvetica, sans-serif;
        border-radius: 10px 10px;
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        flex-wrap: wrap;
        row-gap: 10px;
        column-gap: 30px;
        background-image: url("../imagem/tela-fundo.png");
        background-position: center center;
        background-repeat: no-repeat;
        background-size: cover;
        color: black;
        padding: 16px;
        height: 550px;
        width: 700px;
        
    }

    .btn-group {

    }

   

    .bloco-1 {
        font-size: 1.2em;
        color: white;
        border-radius: 5px 5px;
        border: 2px solid black;
        order: 0;
        flex: 0 1 auto;
       
    }

    .bloco-2 {
        color: white;
        background-color: rgba(39, 39, 41, 0.486);
        border-radius: 10px 10px;
        flex-basis: auto;
        height: 500px;
        width: 400px;
        border: 2px solid black;
        order: 0;
        flex: 0 1 auto;
    }
    .container ul {
       
        list-style-type: none;
        margin: 0;
        padding: 10px;
        text-align: left;
    }
</style>