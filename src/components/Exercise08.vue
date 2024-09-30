<template>
    <div>
      <div>
        <!-- Nút "Tăng dần" -->
        <button @click="sortAscending" :class="{ active: isAscending }">
          Tăng dần
        </button>
  
        <!-- Nút "Giảm dần" -->
        <button @click="sortDescending" :class="{ active: isDescending }">
          Giảm dần
        </button>
      </div>
  
      <!-- Render mảng các số -->
      <div class="numbers">
        <span v-for="(number, index) in numbers" :key="index">
          {{ number }}
        </span>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: "Exercise08",
    data() {
      return {
        // Mảng các số nguyên bất kỳ
        numbers: [5, 2, 9, 1, 5, 6],
        // Biến để kiểm soát trạng thái của nút Tăng dần/Giảm dần
        isAscending: false,
        isDescending: false,
      };
    },
    methods: {
      // Hàm sắp xếp tăng dần
      sortAscending() {
        this.numbers.sort((a, b) => a - b);
        this.isAscending = true;
        this.isDescending = false;
      },
      // Hàm sắp xếp giảm dần
      sortDescending() {
        this.numbers.sort((a, b) => b - a);
        this.isAscending = false;
        this.isDescending = true;
      },
    },
  };
  </script>
  
  <style scoped>
  button {
    padding: 10px;
    margin: 5px;
    font-size: 16px;
    border: 2px solid black;
    cursor: pointer;
    background-color: white;
  }
  
  .active {
    background-color: black;
    color: #fff;
  }
  
  .numbers {
    margin-top: 20px;
  }
  
  .numbers span {
    display: inline-block;
    padding: 10px;
    border: 1px solid #ccc;
    margin: 5px;
    font-size: 18px;
    text-align: center;
    width: 30px;
  }
  </style>
  