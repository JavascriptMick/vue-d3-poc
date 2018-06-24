<template>
  <p>Example3 {{computedMessage}}</p>
</template>

<script lang="ts">
import Vue from 'vue';
import Component from 'vue-class-component';

@Component({
 props:  {
   test1: {type: String, default: () => 'Default Prop'},
   test2: {type: Array, default: () => ['D', 'e', 'f', 'a', 'u', 'l', 't']}
  },
})
export default class ArrayPropsExample3 extends Vue {
  test1: string;
  test2: string[];
  get computedMessage() {
    return this.test1 + ' ' + this.test2;
  }
}
</script>