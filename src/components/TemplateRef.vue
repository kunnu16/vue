<template>
  <div>
    <h1>Template ref</h1>
    <input type="text" class="testclass" ref="input"  />
    <button @click="getInfo">get</button>
  </div>
</template>

<script>
import { ref } from 'vue'
export default {
    name : 'TemplateRef',
    setup() {
        const input = ref(null);
        // input.value.focus();
        const getInfo = () => {
            input.value.focus();
            console.log(input.value);
        }
        return {
            input,
            getInfo
        }
    }
}
</script>

<style>

</style>