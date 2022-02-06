<template>
    <div class="formulario">
        <div class="formulatio-title">Defina a palavra</div>
        <input type="text" class="formulario-input">
        <button>Próximo</button>
    </div>
</template>

<script>
export default {
    name: 'Formulario'
}
</script>

<style scoped>
    .formulario{
        display: flex;
        flex-direction: column;
        align-content: center;
        text-align: center;
        justify-content: center;
        margin-top: 20px;
    }

    .formulario-input{
        padding: 10px 5px;
        border: 0;
        border-radius: 5px;
        margin: 10px 0px;
        color: var(--color-text-dark);
        font-size: 16px;
    }
    
</style>