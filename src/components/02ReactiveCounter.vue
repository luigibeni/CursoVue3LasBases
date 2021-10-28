<template>
  <h2>Reactive Counter</h2>
  <h3>{{ counter }}</h3>
  <h3>{{ counterCoputed }}</h3>
  <button @click="increment">Incrementar</button>
  <button @click="decrement">Decrementar</button>
</template>
<script>
import {reactive, computed, toRefs} from "vue"
export default {
  name: "ReactiveCounter",
  setup() {
    const data = reactive({
      counter: 0,
      counterCoputed: computed(() => {
        return `El valor de counter es ${data.counter}`
      })
    })

    const increment = () => {
      data.counter++
    }

    const decrement = () => {
      data.counter--
    }

    return { ...toRefs(data), increment, decrement}
  }
}
</script>
