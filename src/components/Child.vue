<template>
<div>
    <h1>Child Component! : {{name}}</h1>
    <h2>{{userInfo.userId}} and {{userInfo.email}}</h2>
    <button @click="getData()">getData</button>
</div>
</template>

<script>
export default {
    name: 'Child',
    props: {
        name: String,
        userInfo: Object,
        getData : Function,
    }
}
</script>
