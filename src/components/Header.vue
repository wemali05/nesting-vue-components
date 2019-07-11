<template>
 <header>
  <h1>{{title}}</h1>
  <button v-on:click="changeTitle">change title</button>
 </header>
</template>

<script>


export default {
  props:{
    title:{
      type: String
    }
  },
  data () {
    return {
      title:'Alfred wemali Vue App:)'
    }
  },
  methods:{
    changeTitle(){
      this.title = "Wizards App"
    }
  }
}
</script>

<style scoped>
  header{
    background: lightgreen;
    padding: 10px;
  }
  h1{
    color: #222;
    text-align: center;
  }

</style>
