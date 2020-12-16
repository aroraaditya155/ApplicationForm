<template>
<div>
<div class="form-question">
{{question}}
</div>
<div class="form-answer">
{{answer}}
</div>
</div>
</template>

<script>


export default {
 
 props:{
     question:{
         type:String,
         required:true
     },
     answer:{
         type:Object,
         required:true
     }
 },
  data(){
    return {
      
      
    }
  }

  
}
</script>

<style>
#profile {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  display:flex;
  flex-direction:column;
}
</style>
