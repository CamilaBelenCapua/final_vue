<template>
   <section class="src-components-Input">
     <div class="Input">
      <h3>Color</h3>
        <hr>
        <br>
          <validate tag="div">
            <input 
              type="text"
              id="inputColor"
              name="inputColor" 
              class="form-control"
              autocomplete="off"
              v-model.trim="formData.color" 
            />
          </validate>

          <h3>Fondo</h3>
        <hr>
        <br>
          <validate tag="div">
            <input 
              type="text"
              id="inputFondo"
              name="inputFondo" 
              class="form-control"
              autocomplete="off"
              v-model.trim="formData.fondo" 
            />
          </validate>

          <h3>Size</h3>
        <hr>
        <br>
          <validate tag="div">
            <input 
              type="text"
              id="inputSize"
              name="inputSize" 
              class="form-control"
              autocomplete="off"
              v-model.trim="formData.size" 
            />
          </validate>

          <h3>Enter text</h3>
        <hr>
        <br>
          <validate tag="div">
            <input 
              type="text"
              id="input"
              name="input" 
              class="form-control"
              autocomplete="off"
              v-model.trim="formData.input" 
            />
          </validate>

          <Son  :input="formData.input"
                :color = "formData.color"
                :fondo = "formData.fondo"
                :size = "formData.size"
          ></Son>
        <Answers></Answers>
        <br>
      </div>
  </section>
</template>

<script>
import Son from './InputSon.vue'
import Answers from './Answers.vue'
export default {
  name: 'src-components-Input',
  components : {
      Son,
      Answers
    },
  props: [],
  mounted () {
  },
  
  data () {
    return {
      formData : this.getInicialData()
    }
  },
  methods: {
      getInicialData() {
        return {
          input: '',
          Color: '',
          Fondo: '', 
          Size: ''
        }
      },
  },
  
  computed: {
  },
  
}
</script>

<style scoped>
</style>