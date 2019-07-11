<template>
  <div>
   <app-header v-bind:title="title" v-on:changeTitle="updateTitle($event)"></app-header>
   <app-ninja v-bind:ninjas="ninjas"></app-ninja>
   <app-footer v-bind:title="title" ></app-footer>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
import Ninjas from './components/Ninjas.vue'

export default {
  components:{
    'app-header': Header,
    'app-footer': Footer,
    'app-ninja': Ninjas 
  },
  data () {
    return {
        ninjas: [
                {name: 'Ryu', speciality: 'Vue Components', show: false},
                {name: 'Crystal', speciality: 'HTML Wizardry', show: false},
                {name: 'Hitoshi', speciality: 'Click Events', show: false},
                {name: 'Tango', speciality: 'Conditionals', show: false},
                {name: 'Kami', speciality: 'Webpack', show: false},
                {name: 'Yoshi', speciality: 'Data Diggin', show: false}
            ],
       title: 'Alfred wemali Vue App:)'     
    }
  },
  methods:{
    updateTitle(updateTitle){
      this.title = updateTitle;
    }
  }
}
</script>

<style scoped>

</style>
