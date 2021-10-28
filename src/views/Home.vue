<template>
  <hr />
  <hello-world></hello-world>
  <hr />
  <simple-counter></simple-counter>
  <hr />
  <reactive-counter></reactive-counter>
  <hr />
  <watch-counter></watch-counter>
  <hr />
  <composition-api-counter></composition-api-counter>
  <hr />
  <todo-list></todo-list>
  <hr />
  <simple-fetch></simple-fetch>
  <hr />
  <Suspense>
    <template #default>
      <SuspenseFetch />
    </template>
    <template #fallback>
      cargando informacion de la API, un momento por favor...
    </template>
  </Suspense>
  <hr />
  <profile-with-props name="Luis" age="33" />
</template>

<script>
import HelloWorld from "@/components/00HelloWorld"
import SimpleCounter from "@/components/01SimpleCounter";
import ReactiveCounter from "@/components/02ReactiveCounter";
import WatchCounter from "@/components/03WatchCounter";
import CompositionApiCounter from "@/components/CompositionApiCounter";
import TodoList from "@/components/05TodoList";
import SimpleFetch from "@/components/06SimpleFetch";
import SuspenseFetch from "@/components/07SuspenseFetch";
import ProfileWithProps from "@/components/08ProfileWithProps";
export default {
  name: 'Home',
  components: {
    ProfileWithProps,
    SuspenseFetch,
    SimpleFetch,
    TodoList,
    CompositionApiCounter,
    WatchCounter,
    ReactiveCounter,
    SimpleCounter,
    HelloWorld
  }
}
</script>
