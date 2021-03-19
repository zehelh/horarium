<template>
  <div class="col-12">
    <custom-form @create="addItem"></custom-form>
    <semaine></semaine>
  </div>
</template>

<script>
import CustomForm from './components/CustomForm.vue';
import Semaine from './components/Semaine.vue'

export default {
  name: 'App',
  data(){
    return {
      list: [],
    }
  },
  components: {
    CustomForm,
    Semaine,
  },
  methods: {
    addItem(item) {
      this.list.push(item);
      console.log(this.list);
      console.log('2/4');
    },
  },
  watch: {
    list() {
      console.log('3/4');
      console.log(this.list);
    },
  },
  provide() {
    return {
      list: this.list,
    }
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
