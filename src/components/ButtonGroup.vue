<template>
    <div class="button-group">
      <button @click="handleClick('Horror')">Horror</button>
      <button @click="handleClick('Romantis')">Romantis</button>
      <button @click="handleClick('Action')">Action</button>
    </div>
  </template>
  
  <script>
  export default {
    methods: {
      handleClick(category) {
        this.$emit('update-category', category);
      }
    }
  }
  </script>
  
  <style scoped>
  .button-group {
    margin: 20px 0;
  }
  
  .button-group button {
    background-color: #007BFF;
    color: white;
    border: none;
    padding: 10px 20px;
    margin: 5px;
    cursor: pointer;
    border-radius: 5px;
    font-size: 16px;
    transition: background-color 0.3s ease;
  }
  
  .button-group button:hover {
    background-color: #0056b3;
  }
  </style>
  