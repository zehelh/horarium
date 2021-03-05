<template>
  <div class="col-12">
    <semaine></semaine>
  </div>
</template>

<script>
import Semaine from './components/Semaine.vue'

export default {
  name: 'App',
  components: {
    Semaine
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
