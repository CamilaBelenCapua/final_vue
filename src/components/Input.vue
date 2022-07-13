<template>
   <section class="src-components-Input">
      <span>Color: <input type="text" v-model="color"/></span>
      <span>Fondo: <input type="text" v-model="fondo"/></span>
      <span>Size: <input type="text" v-model="size"/></span>
      <hr>
      <span>Texto: <input type="text" :style="style(color,fondo,size)" v-model="texto"/></span>
      <hr>
      <span>Cantidad de palabras: {{count}}</span>
      <Answers></Answers>
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
      color:"",
      fondo:"",
      size:"",
      texto:""
    }
  },
  methods: {
      style(color,fondo,size){
        return{
          color: color,
          backgroundColor: fondo,
          fontSize: size + "px"
        }
      }
  },
  
  computed: {
    count(){
      let cantidad = this.texto.split(' ')
      return cantidad.length -1
    }
  },
  
}
</script>

<style scoped>
</style>