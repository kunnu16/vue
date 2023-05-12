<template>
<div class="container">
    <h1>Counter</h1>
    <h2 id="counter">{{count}}</h2>

    <div class="button-container">
        <button @click="increaseCount">Increase</button>
        <button v-on:click="decreaseCount">Decrease</button>
    </div>
</div>
</template>

<script>
export default {
    name: "Counter App",
    data() {
        return {
            count: 0,
        }
    },
    methods: {
        increaseCount() {
            this.count++;
        },
        decreaseCount() {
            if (this.count <= 0) {
                this.count = 0;
            } else {
                this.count--;
            }
        }
    }
}
</script>

<style>
.container {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
}

#counter {
    margin: 10px;
    padding: 10px;
}

button {
    margin-right: 5px;
}
</style>
