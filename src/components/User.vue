<template>
<div class="user">
    <h1>{{data.name}}</h1>
    <h1>{{data.email}}</h1>
    <button v-on:click="getName(data.name)">alert</button>
</div>
</template>

<script>
export default {
    name: "User",
    props: {
        data: Object,
        getName:Function
    }
}
</script>

<style >
.user{
    background-color: skyblue;
    padding: 10px;
    margin-bottom: 20px;
    border-bottom: 10px;
}
</style>