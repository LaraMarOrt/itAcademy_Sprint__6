<template>
    <div>
        <button class="btnAnt" @click="$emit('ant')">Anterior</button>
        <button class="btnSeg" @click="$emit('seg')">Siguiente</button>
    </div>
</template>

<script>
export default {
    name: 'Botones',
    emits: ['ant', 'seg'],
    }
</script>

<style scoped>
button {
    margin: 20px;
}

.btnAnt {
    background-color: #989bcd;
    color:#fff;
}
.btnSeg {
    background-color: #989bcd;
    color:#fff;
}

button:hover {
    background-color: #6f2196;
    color:#fff;
}
</style>