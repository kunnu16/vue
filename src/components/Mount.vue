<template>
  <div>
    <h1>beforeMount and after mounted</h1>
    <p>hello World!</p>
  </div>
</template>

<script>
export default {
    name : 'Mount',  
    beforeMount() {
        console.log(".....beforeMount......",this.$el);
    },
    mounted() {
        console.log(".....mounted.......",this.$el);
    }
}
</script>

<style>

</style>