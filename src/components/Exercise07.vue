<template>
    <div>
      
      <button
        v-for="index in 3"
        :key="index"
        :class="{ active: activeIndex === index }"
        @click="setActiveIndex(index)"
      >
        Button {{ index }}
      </button>
    </div>
  </template>
  
  <script>
  export default {
    name: 'Exercise07',
    data() {
      return {
       
        activeIndex: 1
      };
    },
    methods: {
 
      setActiveIndex(index) {
        this.activeIndex = index;
      }
    }
  };
  </script>
  
  <style scoped>

  button {
    padding: 10px;
    margin: 5px;
    font-size: 16px;
    cursor: pointer;
  }
  
  /* Style cho button đang được chọn (active) */
  .active {
    background-color: red;
    color: #fff;
  }
  </style>
  