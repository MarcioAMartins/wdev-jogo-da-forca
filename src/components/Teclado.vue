<template>
    <div class="teclado">
        
        <button
        class="teclado-botao"
        v-for="(letra, key) in 'abcdefghijklmnopqrstuvwxyz'"
        :key="key"
        v-on:click="alert(letra)">
         {{letra}}   
        </button>

    </div>
</template>

<script>

export default {
    name: 'Teclado',    
    props:{
       letras: Array,
       verificaLetra: Function
    },
    
    data(){
        return{
            
        }
    },
}
</script>

<style scoped>

.teclado{
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    width: 85%;
    margin-top: 20px;
}
.teclado-botao{
    margin: 5px;
}
</style>