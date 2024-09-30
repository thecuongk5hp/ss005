<template>
    <div>
      
      <button @click="showMessage">Hiển thị</button>
      
    
      <button @click="hideMessage">Ẩn</button>
  
      
      <div v-show="isVisible" class="notification">
        =))
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'Exercise04',
    data() {
      return {
       
        isVisible: false
      }
    },
    methods: {
     
      showMessage() {
        this.isVisible = true;
      },
    
      hideMessage() {
        this.isVisible = false;
      }
    }
  }
  </script>
  
  <style scoped>
  .notification {
    margin-top: 20px;
    padding: 10px;
    border: 1px solid #ccc;
    background-color: #f4f4f4;
    color: #333;
    font-size: 16px;
  }
  button {
    margin-right: 10px;
    padding: 10px;
    font-size: 16px;
    cursor: pointer;
  }
  </style>
  