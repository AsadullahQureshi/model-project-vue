<template>
   <div class="model">
       <h1>Hello Model with props Vue:) {{ title }}</h1>
       <p>My first Vue App {{ msg }} </p>
       <p>{{ job }}</p>

   </div>
  </template>
  
  <script>
  // import HelloWorld from './components/HelloWorld.vue'
//   import ModelView from './components/ModelComponent.vue'
  export default {
    name: 'App',
    props:['msg','job'],
     data(){
      return{
        title:"Asad Model",
      }
    },
  
  }
  </script>
  
  <style scoped>
  .model {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2cd;
    margin: 60px auto; 
    background-color: rgba(0,0,0, 0.1);
    /* position: 0; */
    width: 567px;
    height: 300px;
    float:center;

  }
  </style>
  