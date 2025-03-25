<template>
    <div class="forca">

        <img :src="`https://raw.githubusercontent.com/william-costa/wdev-hangman-game-resources/master/images/hangman/${erros}.svg`" >

    </div>
</template>

<script>

export default {
    name: 'GameForca',

    props:{
       erros:Number
    },
    
    data(){
        return{
            
        }
    },
}
</script>

<style scoped>
   .forca img{
       height: 100px;
   } 
</style>