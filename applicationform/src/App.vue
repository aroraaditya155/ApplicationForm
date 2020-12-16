<template>
 
  <application-form></application-form>
</template>

<script>
import ApplicationForm from './components/ApplicationForm.vue'



export default {
  name: 'App',
  components: {
   
    ApplicationForm
    
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
