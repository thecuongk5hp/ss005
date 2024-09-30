<template>
    <div>
      <h2>Danh sách các thỏa mãn điều kiện:</h2>
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
        
        numbers: [5,12,15,22,9,18,25,30,7,33]
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
    color: blue;
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
  