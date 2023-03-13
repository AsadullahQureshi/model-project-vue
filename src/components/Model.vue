<template>
  <div class="backdrop">
    <div class="model" :class="{sale:theme==='sale'}">
      <h1>{{ title }}</h1>
      <p>{{ msg }}</p>
      <p>{{ job }}</p>
      <p>{{ location }}</p>
      <slot></slot>
    </div>
  </div>
</template>
  
  <script>
// import HelloWorld from './components/HelloWorld.vue'
//   import ModelView from './components/ModelComponent.vue'
export default {
  name: "App",
  props: ["title",'msg','location', "theme","job"],
  data() {
    return {
      // showModel: false,
    };
  },
  methods:{
    closeModel(){
      this.$emit('close')
    }
  }
};
</script>
  
  <style scoped>
.model {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2cd;
  margin: 100px auto;
  padding: 20px;
  width: 400px;
  background-color:white;
  /* position: 0; */
  height: 300px;
  float: center;
  border-radius:10px;
}
.backdrop{
  top:0;
  position:fixed;
  width: 100%;
  height: 100%;
  background: rgba(0, 0,0, 0.3);
}

.model.sale{
 background-color: crimson;
 color: white;
}
.model .sale, .btn{
  background-color: crimson;

}
</style>
  