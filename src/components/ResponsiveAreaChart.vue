<template>
  <div>
    <h1>Responsive Area Chart (wip){{computedPadded}}</h1>
    <!-- <svg @mousemove="mouseover" :width="width" :height="height">
      <g :style="{transform: `translate(${margin.left}px, ${margin.top}px)`}">
        <path class="area" :d="paths.area" />
        <path class="line" :d="paths.line" />
        <path class="selector" :d="paths.selector" />
      </g>
    </svg> -->
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import Component from 'vue-class-component';

const AppProps = Vue.extend({
  props: {
    // test : Array,

    // data: {
    //   type: Array,
    //   default: () => [],
    // },

    // margin : {
    //   type: Object,
    //   default: () => ({
    //     left: 0,
    //     right: 0,
    //     top: 10,
    //     bottom: 10,
    //   }),
    // },

    // ceil : {
    //   type: Number,
    //   default: 100,
    // },
    // morestuff: { type: Array, default: () => [] },
    stuff: String,
    test: String
  },
});

@Component({
  // props: {
  //   stuff: String,
  // },
})
export default class ResponsiveAreaChart extends AppProps {
// export default class ResponsiveAreaChart extends AppProps {
  // public stuff: string = '';
  // data
  public width =  0;
  public height =  0;
  public paths = {
    area: '',
    line: '',
    selector: '',
  };
  public lastHoverPoint = {};
  public scaled = {
    x: null,
    y: null,
  };
  public animatedData = [];
  public points = [];

  get computedPadded() {
    return 'hello2' + this.stuff;
      // const width = this.width - this.margin.left - this.propMargin.right;
      // const height = this.height - this.propMargin.top - this.propMargin.bottom;
      // return { width, height };
  }
}
</script>
