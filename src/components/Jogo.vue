<template>
    <div class="jogo">

        <Forca
        :erros="erros"
        />

        <Palavra
        :palavra="palavra"
        :dica="dica"
        :verificarLetra="verificarLetra"
        :etapa="etapa"
        />
        <Teclado
        :letras="letras"        
        :verificarLetra="verificarLetra"
        />

    </div>
</template>

<script>
import Forca from './Forca';
import Palavra from './Palavra';
import Teclado from './Teclado';


export default {
    name: 'Jogo',
    components:{
        Forca,
        Palavra,
        Teclado
    },

    props:{
       erros:Number,
       palavra:String,
       dica:String,
       verificarLetra: Function,
       etapa: String,
       letras:Array
    },
    
    data(){
        return{
            
        }
    },

    methods:{
        
    }
}
</script>

<style scoped>
    .jogo{
        width: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;
        text-align: center;
    }
</style>