<template>
    <div class="card card-body semaine d-flex flex-row justify-content-evenly flex-wrap col-12">
      <div class="day lundi col-8 col-md-3 d-flex flex-column">
        <p>Lundi</p>
      </div>
      <div class="day mardi col-8 col-md-3 d-flex flex-column">
        <p>mardi</p>
      </div>
      <div class="day mercredi col-8 col-md-3 d-flex flex-column">
        <p>mercredi</p>
      </div>
      <div class="day jeudi col-8 col-md-3 d-flex flex-column">
        <p>jeudi</p>
      </div>
      <div class="day vendredi col-8 col-md-3 d-flex flex-column">
        <p>vendredi</p>
      </div>
      <div class="day samedi col-8 col-md-3 d-flex flex-column">
        <p>samedi</p>
      </div>
      <div class="day dimanche col-8 col-md-3 d-flex flex-column">
        <p>dimanche</p>
      </div>
    </div>
</template>

<script>
export default {
  name: 'Semaine',
  data(){
    return {

    }
  },
  methods: {

  },
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