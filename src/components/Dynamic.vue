<template>
  <div>
    <h1>Dynamic</h1>
    <button @click="tab = 'CPPVue' ">Load CPP</button>
    <button @click="tab = 'NodeVue' ">Load Node</button>
    <button @click="tab = 'JavascriptVue' ">Load Javascript</button>

    <component :is='tab' />
  </div>
</template>

<script>
import { provide } from 'vue';
import CPPVue from "./CPP.vue";
import JavascriptVue from "./Javascript.vue";
import NodeVue from "./Node.vue";

export default {
  name: "Dynamic",
  components: {
    CPPVue,
    JavascriptVue,
    NodeVue,
  },
  data() {
    return {
      tab : ''
    }
  },
  setup() {
    provide('testing' , 'testvalue');
    provide('grepruby','gammastack')
  }
};
</script>

<style>
</style>
