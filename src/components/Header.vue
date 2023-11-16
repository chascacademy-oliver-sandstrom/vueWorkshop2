
<template>
    <header>
      <h1>{{ title }}</h1>
    </header>
  </template>
  
  <script>
  export default {
    props: {
      title: {
        type: String,
        default: "Your neightbours", 
      },
    },
  };
  </script>
  
  <style scoped>
  header {
    background-color: #333;
    color: white;
    padding: 15px;
    margin: 10px;
  }
  
  h1 {
    margin: 0;
    font-size: 2.5rem;
  }
  </style>
  