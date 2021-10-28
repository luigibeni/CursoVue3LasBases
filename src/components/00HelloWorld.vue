<template>
  <h2>Hola mundo</h2>
  <p>{{ message }}</p>
  <label for="message">Mensaje</label>
  <input id="message" v-model="message" />
</template>
<script>
import { ref } from "vue"
  export default {
    name: 'HelloWorld',
    setup (){
      const message = ref("Hello")
      return { message }
    }
  }
</script>
