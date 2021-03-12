<template>
    <div class="card card-body semaine d-flex flex-row justify-content-evenly flex-wrap col-12">
    <div v-if="list">COUCOU</div>
      <div class="day col-8 col-md-3 d-flex flex-column">
        <p>Lundi</p>
        <div v-if="lundi">
          <div v-for="item in lundi" :key="item"></div>
        </div>
      </div>
      <div class="day col-8 col-md-3 d-flex flex-column">
        <p>mardi</p>
        <div v-if="mardi">
          <div v-for="item in mardi" :key="item"></div>
        </div>
      </div>
      <div class="day col-8 col-md-3 d-flex flex-column">
        <p>mercredi</p>
        <div v-if="mercredi">
          <div v-for="item in mercredi" :key="item"></div>
        </div>
      </div>
      <div class="day col-8 col-md-3 d-flex flex-column">
        <p>jeudi</p>
        <div v-if="jeudi">
          <div v-for="item in jeudi" :key="item"></div>
        </div>
      </div>
      <div class="day col-8 col-md-3 d-flex flex-column">
        <p>vendredi</p>
        <div v-if="vendredi">
          <div v-for="item in vendredi" :key="item"></div>
        </div>
      </div>
      <div class="day col-8 col-md-3 d-flex flex-column">
        <p>samedi</p>
        <div v-if="samedi">
          <div v-for="item in samedi" :key="item"></div>
        </div>
      </div>
      <div class="day col-8 col-md-3 d-flex flex-column">
        <p>dimanche</p>
        <div v-if="dimanche">
          <div v-for="item in dimanche" :key="item"></div>
        </div>
      </div>
    </div>
</template>

<script>
export default {
  // inject: ['list'],
  props: ['list'],
  name: 'Semaine',
  data(){
    return {
      lundi: {},
      mardi: {},
      mercredi: {},
      jeudi: {},
      vendredi: {},
      samedi: {},
      dimanche: {},
    }
  },
  methods: {

  },
  watch: {
    list() {
      console.log('YESSSSSSSSSSSSSSSS');
      console.log(this.list);
      for (const item in this.list) {
        switch (item.days) {
          case 'lundi':
            this.lundi.push(item.data);            
            break;
          case 'mardi':
            this.mardi.push(item.data);            
            break;
          case 'mercredi':
            this.mercredi.push(item.data);            
            break;
          case 'jeudi':
            this.jeudi.push(item.data);            
            break;
          case 'vendredi':
            this.vendredi.push(item.data);            
            break;
          case 'samedi':
            this.samedi.push(item.data);            
            break;
          case 'dimanche':
            this.dimanche.push(item.data);            
            break;        
        }
      }
    }
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