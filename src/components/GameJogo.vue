<template>
    <div class="jogo">

        <GameForca
        :erros="erros"
        />

        <GamePalavra
        :palavra="palavra"
        :dica="dica"
        :verificarLetra="verificarLetra"
        :etapa="etapa"
        />
        <GameTeclado
        v-if="etapa === 'jogo'"
        :letras="letras"        
        :verificarLetra="verificarLetra"
        :jogar="jogar"
        />

        <GameFinal
            v-if="etapa != 'jogo'" 
            :etapa="etapa"
            :texto="etapa === 'ganhador' ? 'Parabéns :)' : 'Tadinho :('"
            :jogarNovamente="jogarNovamente"
        />

    </div>
</template>

<script>
import GameForca from './GameForca';
import GamePalavra from './GamePalavra';
import GameTeclado from './GameTeclado';
import GameFinal from './GameFinal';



export default {
    name: 'GameJogo',
    components:{
        GameForca,
        GamePalavra,
        GameTeclado,
        GameFinal
    },

    props:{
       erros:Number,
       palavra:String,
       dica:String,
       etapa: String,
       letras:Array,
       verificarLetra: Function,
       jogar: Function,
       jogarNovamente: Function

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