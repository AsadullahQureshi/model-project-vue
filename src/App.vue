<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <h1>Hello Vue:) {{ title }}</h1>
  <p>My first Vue App</p>
  <input type="text" v-model="title" ref="name">
  <button @click="changeptag">Click me</button>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  // components: {
  //   HelloWorld
  // }
  data(){
    return{
      title:"Asad",
    }
  },
  methods: {
    changeptag(){
        this.title="Change Through Button"
        console.log(this.$refs.name)
        this.$refs.name.classList.add('form-control')
        this.$refs.name.focus()
    }


  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
