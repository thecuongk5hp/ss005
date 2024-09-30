<template>
    <div>
      <button @click="toggleShow">{{ isShow ? 'Ẩn' : 'Hiện' }}</button>
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
      toggleShow() {
        this.isShow = !this.isShow; 
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
    font-size: 16px;
  }
  </style>
  