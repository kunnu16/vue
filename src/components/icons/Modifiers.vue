<template>
<div>
    <h1>Form Modifiers</h1>
    <input type="number" v-model.lazy.trim="data"/>
    <h2>data is :{{data}}</h2>
    <h2>data is : {{typeof(data)}}</h2>
</div>
</template>

<script>
export default {
    name : "Modifiers",
    data() {
        return {
            data : '',
        }
    }
}
</script>

<style>

</style>
