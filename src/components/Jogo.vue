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
        v-if="etapa === 'jogo'"
        :letras="letras"        
        :verificarLetra="verificarLetra"
        :jogar="jogar"
        />

        <Final
            v-if="etapa != 'jogo'" 
            :etapa="etapa"
            :texto="etapa === 'ganhador' ? 'Parabéns :)' : 'Tadinho :('"
            :jogarNovamente="jogarNovamente"
        />

    </div>
</template>

<script>
import Forca from './Forca';
import Palavra from './Palavra';
import Teclado from './Teclado';
import Final from './Final';



export default {
    name: 'Jogo',
    components:{
        Forca,
        Palavra,
        Teclado,
        Final
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