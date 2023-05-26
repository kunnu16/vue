<template>
  <div>
    <h1>Node</h1>
    <h2>{{first}} ----------- {{second}}</h2>
  </div>
</template>

<script>
import { inject } from 'vue'
export default {
    name : 'Node',
    setup() {
      const first = inject('testing');
      const second = inject('grepruby','kkkkk');

      return {
        first,second
      }
    }
}
</script>

<style>

</style>