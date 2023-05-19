<template>
<div>
    <h1>Hello World!</h1>
    <h1 :class="applyStyle">Class Binding</h1>
    <button v-on:click="color = !color">change</button>


    <!-- ref -->
    <br /><br />
    <input type="text" ref="abc"/>
    <button @click="getData">set</button>
</div>
</template>

<script>
export default {
    name: "ClassBinding",
    data() {
        return {
            color: true
        }
    },
    computed: {
        applyStyle() {
            return {
                yellow: this.color,
                err: true,
                other: true
            }
        }
    },

    methods : {
        getData() {
            this.$refs.abc.focus();
            const val = this.$refs.abc.value;
            console.log(val);
            this.$refs.abc.style.color="red"
        }
    }
}
</script>

<style scoped>
.yellow {
    background-color: yellow;
    width: 200px;
    padding: 10px;
}

.err {
    color: red;
}

.other {
    font-size: 50px;
}
</style>
