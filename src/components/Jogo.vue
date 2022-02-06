<template>
    <div class="jogo">

        <Forca
        :erros="erros"
        />

        <Palavra />

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
       erros:Number
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