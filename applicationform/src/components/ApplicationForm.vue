<template>
  <div>
    <div class="application-form">
      <div v-for="section in newObj" :key="section.sectionNumber" >
        <form-section :section="section"></form-section>
      </div>
    </div>
  </div>
</template>

<script>

import FormSection from './FormSection.vue';

export default {
  components: {  FormSection },

  props: {
    sectionList: [
      {
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
        sectionNumber: { type: Number },
      },
    ],
  },
  data() {
    return {
      newObj: {},
    };
  },
  mounted() {
    this.newObj = [
      {
        heading: "Section 1",
        content: "something something",
        questionAndAnswer: [
          { question: "Q1fddf", answer: "A1" },
          { question: "Q2", answer: "A2" },
        ],
        sectionNumber:1
      },
      {
        heading: "Section 2",
        content: "something something for the section2",
        questionAndAnswer: [
          { question: "Q1", answer: "A1" },
          { question: "Q2", answer: "A2" },
        ],
        sectionNumber:2
      },
    ];
  },
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
