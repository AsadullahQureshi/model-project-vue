<template>
  <div class="backdrop" @click.self="closeModel">
    <div class="model" :class="{sale:theme==='sale'}" @click="closeModel">
      <h1>{{ title }}</h1>
      <p>{{ msg }}</p>
      <p>{{ job }}</p>
      <p>{{ location }}</p>
      <div class="actions">
         <slot name="links"></slot>
        <!-- <slot></slot> -->
      </div>

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
.backdrop{
  top:0;
  position:fixed;
  width: 100%;
  height: 100%;
  background: rgba(0, 0,0, 0.3);
}
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

.model.sale {
 background: crimson;
 color: white;
}

</style>
  