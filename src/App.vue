<template>
  <div id="app">
    <HelloWorld msg="Welcome to My World" />
    <div class="row">
      <div class="col-6">
        <img alt="Vue logo" src="./assets/44544.png" />
        <h1>{{total1}}</h1>
      </div>
      <div class="col-6">
        <img alt="Vue logo" src="./assets/331120.jpg" />
        <h1>{{total2}}</h1>
      </div>
      <div class="col-6">
        <Counter @cc="sum" />
      </div>
      <div class="col-6">
        <Counter @cc="sum1" />
      </div>
    </div>
    <hr />
    <!----ชื่อ สกึล รหัส GPA--->
    ชื่อ-นามสกุล
    <input type="text" v-model="name" />
    รหัสนักศึกษา
    <input type="text" v-model="code" />
    GPA
    <input type="number" v-model="gpa" step="0.01" />
    <hr />
    {{name}} {{code}} {{gpa}}
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import Counter from "./components/Counter.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
    Counter,
  },

  data: function () {
    return {
      total1: 0,
      total2: 0,
      name: "",
      code: "",
      gpa: 0.1,
    };
  },
  methods: {
    sum(counterValue) {
      this.total1 = counterValue;
    },
    sum1(counterValue) {
      this.total2 = counterValue;
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
</style>
