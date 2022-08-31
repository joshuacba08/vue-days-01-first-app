<template>
  <div class="app-container">
    <Saludo />
  </div>
</template>

<script>
  //importaciones
import Count from './components/Count.vue';
import Saludo from './components/Saludo.vue';

//exportaciones o declaraciones
export default {
  name: 'App',
  components: {
    Count,
    Saludo

}
}
</script>

<style>
  .app-container{
    min-height: 100vh;
    background-color: rgb(20, 0, 38);
    color:aliceblue;
  }
</style>
