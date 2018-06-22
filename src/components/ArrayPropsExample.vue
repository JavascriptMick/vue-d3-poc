<template>
  <p>Whats going on? {{computedMessage}}</p>
</template>

<script lang="ts">
import Vue from 'vue';
import Component from 'vue-class-component';

const AppProps = Vue.extend({
  props: {
    test1: String,
    test2: Array,
  },
});

@Component({})
export default class ArrayPropsExample extends AppProps {
  get computedMessage() {
    return this.test1 + ' ' + this.test2;
  }
}
</script>
