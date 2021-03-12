<template>
  <div class="col-12">
    <custom-form @create="addItem" @item="customItem"></custom-form>
    <semaine :list="list"></semaine>
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
      this.list.push('ca add');
      this.list.push(item);
    },
  },
  watch: {
    list() {
      console.log('tkt');
      console.log(this.list);
    },
  },
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
