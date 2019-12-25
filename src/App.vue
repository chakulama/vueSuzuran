<template>
  <div id="app">
    <Home v-bind:tasks="tasks" />
  </div>
</template>

<script>
import Home from './components/Home.vue'

export default {
  name: 'app',
  data(){
    return{
         tasks: [
          { Title: "Kitchen", name: 'Binod', done: true },
          { Title: "Salon", name: 'Yenji', done: false },
          { Title: "BathRoom", name: 'Santi', done: false },
          { Title: "Basura", name: 'Sangey', done: false },
          { Title: "Doorway", name: 'Unis', done: false },
        ]
    }
},
  components: {
    Home
  }
 
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
