<template>
  <div id="app">
    <img src="./assets/logo.png" class="logo-img">
    <img src="./assets/typescript.svg" class="logo-img">
    <img src="./assets/d3-black.png" class="logo-img">
    <HelloWorld msg="Vue.js + TypeScript + D3 Proof of concept"/>
    <!-- <ResponsiveAreaChart stuff="propsthing" /> -->
    <ArrayPropsExample test1="hello" :test2="testArray"/>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import HelloWorld from './components/HelloWorld.vue';
import ResponsiveAreaChart from './components/ResponsiveAreaChart.vue';
import ArrayPropsExample from './components/ArrayPropsExample.vue';

@Component({
  components: {
    HelloWorld,
    ResponsiveAreaChart,
    ArrayPropsExample
  },
})
export default class App extends Vue {
  private testArray: string[] = ['a', 'b', 'c'];
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.logo-img {
  width: 200px;
  height: 200px;
}
</style>
