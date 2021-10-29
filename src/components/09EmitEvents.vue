<template>
  <h2>Emit Events</h2>
  <label for="newMessage">Mensaje</label>
  <input id="newMessage" v-model="message" />
  <button @click="$emit('onFire', message)">Notificar</button>
</template>

<script>
import { ref } from "vue";
export default {
  name: "EmitEvents",
  emits: ["onFire"],
  setup(props, { emit }){
    const message = ref("")
    const notify = () => {
      emit("onFire", message.value)
    }
  }
}
</script>

