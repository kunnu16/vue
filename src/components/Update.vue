<template>
  <div>
    <h1>beforeUpdate and after updated</h1>
    <h1 ref="counter">{{ count }}</h1>

    <button @click="count++">click me</button>
  </div>
</template>

<script>
export default {
  name: "Update",
  data() {
    return {
      count: 0,
    };
  },
  beforeUpdate() {
    console.log("beforeUpdate : ", this.$refs["counter"].textContent);
  },
  updated() {
    console.log("after updated : ", this.$refs["counter"].textContent);
  },
};
</script>

<style>
</style>
