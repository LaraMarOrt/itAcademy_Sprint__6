<script>
import Escena from './Escena.vue'
import Botones from './Botones.vue'
import Inicio from './Inicio.vue'

export default {
  name: 'Home',
  components: { Escena, Botones, Inicio },
  props: ['active'],
  data() {
    return {
      // Ejercicio 1, 2, 3, 4 y 5
      // frases: [
      //   "El nostre heroi estava surant per l'espai sideral quan a la llunyania va albirar una nau espacial",

      //   "Sentia curiositat per l'interior de la nau i es va posar a inspeccionar-la. Va arribar a una sala amb dues portes.",

      //   "L'heroi va decidir travessar la porta que el portava a casa",

      //   "Mentrestant, altres herois no van tenir tanta sort en la seva elecció ..."],

      // Ejercicio 6
      frases: [
        {
          text: "El nostre heroi estava surant per l'espai sideral quan a la llunyania va albirar una nau espacial",
          img: "/1.jpg"
        },
        {
          text: "Sentia curiositat per l'interior de la nau i es va posar a inspeccionar-la. Va arribar a una sala amb dues portes",
          img: "/2.jpg"
        },
        {
          text: "L'heroi va decidir travessar la porta que el portava a casa",
          img: "/3.jpg"
        },
        {
          text: "Mentrestant, altres herois no van tenir tanta sort en la seva elecció ...",
          img: "/4.jpg"
        }
      ],
      currentSentence: 0,
      mostrar: false,
    }
  },
  methods: {
    pasarAnt() {
      if (this.currentSentence > 0) {
        this.currentSentence--;
      }
    }
    ,
    pasarSeg() {
      if (this.currentSentence < this.frases.length - 1) {
        this.currentSentence++;
      }
    }
  }
}

</script>

<template>
  <!-- Ejercicio1
  <Escena></Escena> -->

  <!-- Ejercicio 5 -->
  <div v-if="!mostrar">
    <Inicio @ini="mostrar = true"></Inicio>
  </div>

  <!-- Ejercicio 6  -->
  <div v-if="mostrar" class="backImage" :style="{ backgroundImage: `url(${frases[currentSentence].img})` }">
    <Botones @ant="pasarAnt" @seg="pasarSeg"></Botones>

    <!-- Ejercio 1, 2, 3, 4 y 5 -->
    <Escena :textos="frases" :activeItem="currentSentence"></Escena>
  </div>
</template>

<style scoped>
/* Imagen de fondo */
.backImage {
  width: 100vw;
  height: 100vmin;
  background-size: cover;
}
</style>
