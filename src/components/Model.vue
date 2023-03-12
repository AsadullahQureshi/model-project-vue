<template>
   <div class="model">
       <h1>Hello Model Vue:) {{ title }}</h1>
       <p>My first Vue App</p>

   </div>
  </template>
  
  <script>
  // import HelloWorld from './components/HelloWorld.vue'
//   import ModelView from './components/ModelComponent.vue'
  export default {
    name: 'App',
     data(){
      return{
        title:"Asad Model",
      }
    },
  
  }
  </script>
  
  <style>
  .model {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2cd;
    margin-top: 60px;
  }
  </style>
  