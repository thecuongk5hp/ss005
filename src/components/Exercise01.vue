<template>
    <div>
      <button @click="showMessage">Click Me</button>
      <p v-if="isShow">Rikkei Education</p>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        isShow: false, 
      };
    },
    methods: {
      showMessage() {
        this.isShow = true; 
      },
    },
  };
  </script>
  
  <style scoped>
  button {
    padding: 10px 20px;
    background-color: #4CAF50;
    color: white;
    border: none;
    cursor: pointer;
  }
  
  p {
    font-size: 18px;
    color: #c11818;
  }
  </style>
  