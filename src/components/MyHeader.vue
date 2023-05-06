<template>
  <div>
      <h1> {{Title}} </h1>
      <!-- <h4> {{authorName}} </h4>
      <h4> {{yourName}} </h4> -->
  </div>
  </template>
  
  <script>
  
  export default{ // Exporting Default Object
      name: 'MyHeader',
      props:{ 
  
          Title:String,
        //   bookName:String,
        //   yourName: String
      }
  }
  
  </script>
  
  <style scoped>
  @import url('https://fonts.googleapis.com/css2?family=Bruno+Ace+SC&display=swap');
  div{
      text-align: center;
  }
  h1{
    font-family: 'Bruno Ace SC', cursive;
    font-size: 56px;
    color: white;
  }
  
  </style>