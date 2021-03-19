<template>
      <div class="col-10 d-flex flex-column align-items-center mb-4">
      <button class="btn btn-primary mb-3" type="button" data-bs-toggle="collapse" data-bs-target="#collapseExample" aria-expanded="false" aria-controls="collapseExample">
        Ajouter un évenement
      </button>
      <div class="collapse" id="collapseExample">
        <div class="input-group mb-3">
          <span class="input-group-text" id="basic-addon1">Nom de l'évenement</span>
          <input type="text" class="form-control" v-model="name">
        </div>
        <div class="input-group mb-3">
          <span class="input-group-text" id="basic-addon1">Plage hoaire du debut</span>
          <input type="time" class="form-control" v-model="start">
        </div>
        <div class="input-group mb-3">
          <span class="input-group-text" id="basic-addon1">Plage horaire de fin</span>
          <input type="time" class="form-control" v-model="end">
        </div>
        <div class="btn-group" role="group" aria-label="Basic checkbox toggle button group">
          <input type="checkbox" class="btn-check" v-model="lundi" id="lundi" autocomplete="off">
          <label class="btn btn-outline-primary" for="lundi">Lundi</label>

          <input type="checkbox" class="btn-check" v-model="mardi" id="mardi" autocomplete="off">
          <label class="btn btn-outline-primary" for="mardi">Mardi</label>

          <input type="checkbox" class="btn-check" v-model="mercredi" id="mercredi" autocomplete="off">
          <label class="btn btn-outline-primary" for="mercredi">Mercredi</label>

          <input type="checkbox" class="btn-check" v-model="jeudi" id="jeudi" autocomplete="off">
          <label class="btn btn-outline-primary" for="jeudi">Jeudi</label>

          <input type="checkbox" class="btn-check" v-model="vendredi" id="vendredi" autocomplete="off">
          <label class="btn btn-outline-primary" for="vendredi">Vendredi</label>

          <input type="checkbox" class="btn-check" v-model="samedi" id="samedi" autocomplete="off">
          <label class="btn btn-outline-primary" for="samedi">Samedi</label>

          <input type="checkbox" class="btn-check" v-model="dimanche" id="dimanche" autocomplete="off">
          <label class="btn btn-outline-primary" for="dimanche">Dimanche</label>
        </div>
      <button class="btn btn-primary col-6 mt-3 mb-3" @click="addEvent" >Créer</button>
      </div>
    </div>
</template>

<script>
export default {
  emits: ['create', 'item'],
  name: 'Semaine',
  data(){
    return {
      name: '',
      start: '08:00',
      end: '12:00',
      lundi: false,
      mardi: false,
      mercredi: false,
      jeudi: false,
      vendredi: false,
      samedi: false,
      dimanche: false,
    }
  },
  methods: {
    addEvent() {
      if(this.start != '' && this.end != '' && this.name != '' ){
        let item = {};
        if(this.lundi){
          item.lundi = {
              name: this.name,
              start: this.start,
              end: this.end,
          };
        }
        if(this.mardi){
          item.mardi = {
              name: this.name,
              start: this.start,
              end: this.end,
          };
        }
        if(this.mercredi){
          item.mercredi = {
              name: this.name,
              start: this.start,
              end: this.end,
          };
        }
        if(this.jeudi){
          item.jeudi = {
              name: this.name,
              start: this.start,
              end: this.end,
          };
        }
        if(this.vendredi){
          item.vendredi = {
              name: this.name,
              start: this.start,
              end: this.end,
          };
        }
        if(this.samedi){
          item.samedi = {
              name: this.name,
              start: this.start,
              end: this.end,
          };
        }
        if(this.dimanche){
          item.dimanche = {
              name: this.name,
              start: this.start,
              end: this.end,
          };
        }
        this.$emit('create', item);
      }
    },
  },
  watch: {
  },
  // provide() {
  //   return {
  //     addEvent: this.addEvent,
  //   }
  // }
}
</script>


<style scoped>
  .semaine {
    box-sizing: border-box;
  }
  .day {
    min-height: 30vh;
    box-sizing: border-box;
    border: 1px solid lightgray;
    border-radius: 3px;
    margin: 20px 5px;
    padding: 10px;
  }
</style>