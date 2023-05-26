<template>
  <div>
    <h1>Hello World!  beforeCreate and after created {{name}}</h1>
  </div>
</template>

<script>
export default {
    name : 'Created',
    data() {
        console.log("..............created.................");
        return {
            name:'Kunal',
        }
    },
    beforeCreate() {
        this.name = 'parmar'
        // console.log("jooooooooooooooooooooooo");
        alert("beforeCreate");
    },
    created() {
        this.name = 'parmar'
        alert("created");
        this.name = 'Kunal'
    }

}
</script>

<style>

</style>