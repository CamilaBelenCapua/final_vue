<template>
   <section class="src-components-Input">
    <div>
    <hr>
        <br>
          <br>
            <h5> Cantidad:  {{countLetters}}</h5>
          <br>
        <br>
      </div>
  </section>
</template>

<script>

export default {
  name: 'src-components-Input',
  props: ['input','color', 'fondo', 'size'],
  mounted () {
  },
  
  data () {
    return {}
  },
  methods: {
  },
  
  computed: {
    countLetters(){
      return this.input.length;
    },

    cambiarColor(){
        return 0
    },

    cambiarFondo(){
        return 0
    },

    cambiarSize(){
        return 0
    }


  },
  
}
</script>

<style scoped>
</style>