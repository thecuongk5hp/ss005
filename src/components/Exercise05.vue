<template>
    <div>
      <h2>Danh sách các số chẵn:</h2>
      <ul>
        
        <li v-for="(number, index) in evenNumbers" :key="index">
          {{ number }}
        </li>
      </ul>
    </div>
  </template>
  
  <script>
  export default {
    name: 'Exercise05',
    data() {
      return {
       
        numbers: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
      };
    },
    computed: {
      
      evenNumbers() {
        return this.numbers.filter(number => number % 2 === 0);
      }
    }
  };
  </script>
  
  <style scoped>
  h2 {
    color: green;
  }
  ul {
    list-style-type: none;
    padding: 0;
  }
  li {
    font-size: 18px;
    margin: 5px 0;
  }
  </style>
  