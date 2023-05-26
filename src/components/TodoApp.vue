<template>
<div>
    <div class="Info">
        <label for="Id">Add New Todo :</label>
        <input type="text" placeholder="add new todo" v-model.trim="todoText" id="Id" class="item">
        <button v-if="todoText.length !== 0 " v-on:click="addTodo()">Add</button>
    </div>

    <DisplayTodoVue :todos="todos" :removeTodo="removeTodo" />
</div>
</template>

<script>
import DisplayTodoVue from './DisplayTodo.vue';

export default {
    name: 'TodoApp',
    components: {
        DisplayTodoVue,
    },
    data() {
        return {
            todos: [],
            todoText: '',
            todoId: 0
        }
    },
    methods: {
        addTodo() {
            this.todos.push({
                todoId: this.todoId++,
                todo: this.todoText
            });
            this.todoText = '';
        },
        removeTodo(index) {
            this.todos.splice(index, 1);
        }

    }
}
</script>

<style scoped>
button {
    margin-left: 20px;
}

.item {
    margin-left: 10px;
}
</style>
