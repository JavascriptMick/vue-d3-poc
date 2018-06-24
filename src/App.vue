<template>
  <div id="app">
    <img src="./assets/logo.png" class="logo-img">
    <img src="./assets/typescript.svg" class="logo-img">
    <img src="./assets/d3-black.png" class="logo-img">
    <HelloWorld msg="Vue.js + TypeScript + D3 Proof of concept"/>
    <!-- <ResponsiveAreaChart stuff="propsthing" /> -->
    <h1>Both specified</h1>
    <ArrayPropsExample1 test1="Overrided Prop" :test2="['o', 'v', 'e']"/>
    
    <h1>Test1 (string) specified</h1>
    <ArrayPropsExample1 test1="Overrided Prop"/>
    
    <h1>Test2(Array) specified</h1>
    <ArrayPropsExample1 :test2="['o', 'v', 'e']"/>
    
    <h1>None specified</h1>
    <ArrayPropsExample1/>

    <h1>Violate the type contract (array of strings in Test2)</h1>
    <ArrayPropsExample1 :test2="[1, 2, 3]"/>
    
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import HelloWorld from './components/HelloWorld.vue';
import ResponsiveAreaChart from './components/ResponsiveAreaChart.vue';
import ArrayPropsExample1 from './components/ArrayPropsExample1.vue';
// import ArrayPropsExample2 from './components/ArrayPropsExample2.vue';
// import ArrayPropsExample3 from './components/ArrayPropsExample3.vue';
// import ArrayPropsExample4 from './components/ArrayPropsExample4.vue';

@Component({
  components: {
    HelloWorld,
    ResponsiveAreaChart,
    ArrayPropsExample1,
    // ArrayPropsExample2,
    // ArrayPropsExample3,
    // ArrayPropsExample4
  },
})
export default class App extends Vue {
  // private testArray: string[] = ['a', 'b', 'c'];
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
