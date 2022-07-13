<template>
   <section class="src-components-InputSon">
     
      <span>Cantidad de palabras: {{count}}</span>
  </section>
</template>

<script>
export default {
  name: 'src-components-InputSon',
  components : {
    },
  props: ['input'],
  mounted () {
  },
  
  data () {
   return {}
  },
  methods: {
  },
  
  computed: {
    count(){
      let cantidad = this.input.split(' ')
      return cantidad.length
    }
  },
  
}
</script>

<style scoped>
</style>
