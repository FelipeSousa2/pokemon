<template>
    <header>
        <h1>Catálogo pokemons</h1>
        
    </header>
    <div class="container">
        <div class="bloco-1">
          
            <ul>
                
                <li v-for="item in pokemons"  :key="item.   name">
                    {{item.name}}
                </li>
                
            </ul>
           
        </div>
        
       
        <div class="bloco-2">
            
            <div class="img">
               
                <img
                src="https://raw.githubusercontent.com/PokeApi/sprites/master/sprites/pokemon/17.png" alt="item.name"
                >
            </div>
            
            
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
    @import url('https://fonts.googleapis.com/css2? family=Rubik+Iso & display=swap');

    template {
        font-family: Arial, Helvetica, sans-serif;
    }

    header > h1 {
        font-family: 'Rubik Iso', cursiva;
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

    

    .bloco-1 {
        font-family: 'Rubik Iso', cursiva;
        background-color: rgba(39, 39, 41, 0.486);
        font-size: 1.2em;
        color: white;
        border-radius: 5px 5px;
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
        order: 0;
        flex: 0 1 auto;
    }

    .img {
        border-radius: 5px 5px;
        border: 1px solid white;
        margin: auto;
        width: 90%;
        margin-top: 40px;
        height: 45%;
    }

    img {
        height: 30vh;
       
        margin-top: 25px;
        width: 70%;
    }

    .container ul {
        list-style-type: none;
        margin: 0;
        padding: 10px;
        text-align: left;
    }
</style>