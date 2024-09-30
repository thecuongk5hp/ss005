<template>
    <div>
      <h1>User Role: {{ userRole }}</h1>
      <p>{{ userPermissions }}</p>
    </div>
  </template>
  
  <script>
  export default {
    name: 'Exercise03',
    data() {
      return {
        
        userRole: 'admin' 
      }
    },
    computed: {
      userPermissions() {
        if (this.userRole === 'admin') {
          return 'You have full access.';
        } else if (this.userRole === 'user') {
          return 'You have limited access.';
        } else if (this.userRole === 'guest') {
          return 'You have guest access.';
        } else {
          return 'Invalid role.';
        }
      }
    }
  }
  </script>
  
  <style scoped>
  h1 {
    color: blue;
  }
  </style>
  