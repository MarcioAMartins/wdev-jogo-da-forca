<template>
    <div class="jogo">

        <Forca
        :erros="erros"
        />

        <Palavra
        :palavra="palavra"
        :dica="dica"
        :verificarLetra="verificarLetra"
        />

    </div>
</template>

<script>
import Forca from './Forca';
import Palavra from './Palavra';

export default {
    name: 'Jogo',
    components:{
        Forca,
        Palavra
    },

    props:{
       erros:Number,
       palavra:String,
       dica:String,
       verificarLetra: Function
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