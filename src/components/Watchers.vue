<template>
  <div>
    <h1>Watcher</h1>
    <h2>{{ count }}</h2>
    <button @click="count++">inc</button>
    <button @click="count--">dec</button>
  </div>
</template>

<script>
export default {
  name: "Watchers",
  data() {
    return {
      count: 0,
    };
  },
  watch: {
    count(val,old) {
      if(val > 5 && val>old )this.count= -1;
    },
  },
};
</script>

<style>
</style>