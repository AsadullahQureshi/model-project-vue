<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <h1>Hello Vue:) {{ title }}</h1>
  <p>My first Vue App</p>
  <input type="text" v-model="title" ref="name" />
  <button @click="changeptag">Click me</button>
  <h5>Welcome Model</h5>
  <button @click.alt="toggleModel">Open (alt)</button>

  <h5>Welcome Model 2</h5>
  <button @click="toggleModel2">Open 2</button>
  <div v-if="showModel">
    <ModelView
      :msg="msg"
      :title="title"
      :location="location"
      theme="sales"
      @close="toggleModel"
    >
      <template v-slot:links>
        <a class="btn" href="#">Yes</a>
        <p>Hello this is actions</p>
      </template>
    </ModelView>
  </div>
<teleport to='#model'>


  <div v-if="showModel2">
    <ModelView
      :msg="msg"
      :title="title"
      :location="location"
      theme="sales"
      @close="toggleModel2"
    />
  </div>
  </teleport>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import ModelView from "./components/Model.vue";
export default {
  name: "App",
  components: {
    // HelloWorld
    ModelView,
  },
  data() {
    return {
      msg: "Asad",
      title: "Laravel Full Stack developer",
      location: "Ideafist",
      showModel: false,
      showModel2: false,
    };
  },
  methods: {
    changeptag() {
      this.title = "Change Through Button";
      console.log(this.$refs.name);
      this.$refs.name.classList.add("form-control");
      this.$refs.name.focus();
    },
    toggleModel() {
      this.showModel = !this.showModel;
    },
    toggleModel2() {
      this.showModel2 = !this.showModel2;
    },
  },
};
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

.sale .btn {
  color: white;
  background: red;
  text-decoration: none;
  padding: 10px 10px 10px 10px;
  border-radius: 2px;
  border: 1px solid white;
}
.btn {
  color: saddlebrown;
  background: aliceblue;
  text-decoration: none;
  padding: 10px 10px 10px 10px;
  border-radius: 2px;
  border: 1px solid white;
}
.btn :hover {
  background: white;
  border: 2px solid saddlebrown;
}
</style>
