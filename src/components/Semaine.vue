<template>
    <div class="card card-body semaine d-flex flex-row justify-content-evenly flex-wrap col-12">
      
      <div class="day col-8 col-md-3 d-flex flex-column">
        <p class="bg-light">Lundi</p>
          <div v-for="item in list" :key="item">
            <div v-if="item.lundi">
              <div class="card">
                <div class="card-header bg-primary">{{item.lundi.name}}</div>
                <div class="card-body">De {{item.lundi.start}} à {{item.lundi.end}}</div>
              </div>
            </div>
          </div>
      </div>
      <div class="day col-8 col-md-3 d-flex flex-column">
        <p class="bg-light">mardi</p>
          <div v-for="item in list" :key="item">
            <div v-if="item.mardi">
              <div class="card">
                <div class="card-header bg-primary">{{item.mardi.name}}</div>
                <div class="card-body">De {{item.mardi.start}} à {{item.mardi.end}}</div>
              </div>
            </div>
          </div>
      </div>
      <div class="day col-8 col-md-3 d-flex flex-column">
        <p class="bg-light">mercredi</p>
          <div v-for="item in list" :key="item">
            <div v-if="item.mercredi">
              <div class="card">
                <div class="card-header bg-primary">{{item.mercredi.name}}</div>
                <div class="card-body">De {{item.mercredi.start}} à {{item.mercredi.end}}</div>
              </div>
            </div>
          </div>
      </div>
      <div class="day col-8 col-md-3 d-flex flex-column">
        <p class="bg-light">jeudi</p>
          <div v-for="item in list" :key="item">
            <div v-if="item.jeudi">
              <div class="card">
                <div class="card-header bg-primary">{{item.jeudi.name}}</div>
                <div class="card-body">De {{item.jeudi.start}} à {{item.jeudi.end}}</div>
              </div>
            </div>
          </div>
      </div>
      <div class="day col-8 col-md-3 d-flex flex-column">
        <p class="bg-light">vendredi</p>
          <div v-for="item in list" :key="item">
            <div v-if="item.vendredi">
              <div class="card">
                <div class="card-header bg-primary">{{item.vendredi.name}}</div>
                <div class="card-body">De {{item.vendredi.start}} à {{item.vendredi.end}}</div>
              </div>
            </div>
          </div>
      </div>
      <div class="day col-8 col-md-3 d-flex flex-column">
        <p class="bg-light">samedi</p>
          <div v-for="item in list" :key="item">
            <div v-if="item.samedi">
              <div class="card">
                <div class="card-header bg-primary">{{item.samedi.name}}</div>
                <div class="card-body">De {{item.samedi.start}} à {{item.samedi.end}}</div>
              </div>
            </div>
          </div>
      </div>
      <div class="day col-8 col-md-3 d-flex flex-column">
        <p class="bg-light">dimanche</p>
          <div v-for="item in list" :key="item">
            <div v-if="item.dimanche">
              <div class="card">
                <div class="card-header bg-primary">{{item.dimanche.name}}</div>
                <div class="card-body">De {{item.dimanche.start}} à {{item.dimanche.end}}</div>
              </div>
            </div>
          </div>
      </div>

    </div>
</template>

<script>
export default {
  inject: ['list'],
  name: 'Semaine',
  data(){
    return {
    }
  },
  methods: {

  },
  computed: {
  },
  watch: {
  }
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