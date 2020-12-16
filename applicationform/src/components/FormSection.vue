<template>
<div>
<div class="form-section">
<h1>{{section.heading}}</h1>
<p>{{section.content}}</p>
<div  v-for="Qa in section.questionAndAnswer" :key="Qa.order" class="question-answer">

    <form-question :question="Qa.question" :answer="Qa.answer"> </form-question>
</div>
</div>

</div>
</template>

<script>
import FormQuestion from "./FormQuestion.vue";

export default {
  components: { FormQuestion },

  props: {
    section: {
      heading: {
        type: String,
        required: false,
      },
      content: {
        type: String,
        required: false,
      },
      questionAndAnswer: [
        { question: { type: String } },
        { answer: { type: String } },
        { order: { type: Number } },
      ],
    },
  },
  data(){
      return{
      newObj:{
          
      }}
  },
  mounted() {
   
    
    // this.newObj = {
    //   heading: "Section 1",
    //   content: "something something",
    //   questionAndAnswer: [{question:"Q1fddf",answer:"A1"},{question:"Q2",answer:"A2"}]
    // }
    
  }
};
</script>

<style>
#profile {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  display: flex;
  flex-direction: column;
}
</style>
