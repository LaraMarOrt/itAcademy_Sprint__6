<template>
    <div>
        <h2>Bienvenid@</h2>
        <div>
            Esta es una pequeña historia en la que podrás navegar mediante dos botones (<strong>"Anterior"</strong> y <strong>"Siguiente"</strong>) para
            descubrir la historia de un héroe.
            <div>
                <button @click="$emit('ini')">Comenzar</button>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Inicio',
    emits: ['ini'],
}
</script>

<style scoped>
h2 {
    margin-bottom: 3rem;
}

button {
    background-color: #6f2196;
    color: #fff;
    margin-top: 3rem;
}

button:hover {
    background-color: #989bcd;
}
</style>