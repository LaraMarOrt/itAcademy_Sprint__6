<template>
  <!-- Resolución del ejercicio1
  <div>
    El nostre heroi estava surant per l'espai sideral quan a la llunyania va albirar una nau espacial
  </div> -->

  <!-- Resolución de los ejercicios 2, 3, 4 y 5 (primera aproximación sin imágenes) -->
  <!-- <div class="lineas" :class="{ active: index === activeItem}" v-for="(frase, index) in textos" :key="index"> -->

  <!-- Ejercicio 6, con imágenes -->
  <div v-for="(frase, index) in textos" :image="frase.img" :key="index">
    <div class="lineas" :class="{ active: index === activeItem }">
      {{ frase.text }}
    </div>
  </div>
</template>

<script>
export default {
  name: 'Escena',
  props: ['textos', 'activeItem'],
}

</script>

<style scoped>
.lineas {
  border: 1px solid black;
  border-radius: 15px;
  padding: 10px;
  margin: 20px;
  background-color: rgba(240, 248, 255, 0.801);
}

.active {
  background-color: #eec3c3de;
}
</style>