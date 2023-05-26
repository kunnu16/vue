<template>
<div>
    <ul class="space">
        <li v-for="(item,index) in todos" :key="item.id" class="Info" >
            {{index}} - {{item.todo}}
            <button @click="removeTodo(index)">remove</button>
        </li>
    </ul>
</div>
</template>

<script>
export default {
    name: 'DisplayTodo',
    props: {
        todos: Array,
        removeTodo:Function
    }
}
</script>

<style scoped>
   button{
    margin-left: 20px;
   }
   .Info{
    margin-top: 5px;
    row-gap: 5px;
    justify-content: space-between;
}

</style>
