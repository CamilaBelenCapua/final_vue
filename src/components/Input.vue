<template>
   <section class="src-components-Input">
    <div>
     <span>color: <input type="text" v-model="color" /></span>
     <span>fondo: <input type="text" v-model="fondo" /> </span>
     <span>size:<input type="number" v-model="size" /></span>
    
     <span> texto: 
      <input
        type="text"
        v-model = "texto"
        :style="estiloTexto(color, fondo, size)"
        class="text-center"/>
      </span>

      <p>Cantidad de palabras: {{ count() }}</p>

        <Answers></Answers>
        <br>
      </div>
  </section>
</template>

<script>
import Answers from './Answers.vue'

export default {
  name: 'src-components-Input',
  components : {
      Answers
    },
  props: [],
  mounted () {
  },
  
  data () {
    return {
      color: "",
      fondo: "",
      size: "",
      texto: "Ingrese Texto Aqui",
      
    }
  },
  methods: {
    estiloTexto(color, fondo, size) {
      return `background: ${fondo}; color:  ${color}; width:  ${size}px `;
    }
  },

  
  computed: {
    count() {
      let count = this.texto.split(" ").length;
      return count;
    },
  },
  
}
</script>

<style scoped>
</style>