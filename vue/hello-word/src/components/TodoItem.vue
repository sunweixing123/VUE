<template>
    <div id="todo-list-example">
        <form v-on:submit.prevent="addNewTodo">
            <label for="new-todo">Add a todo</label>
            <input
            id="new-todo"
            placeholder="E.g. Feed the cat"
            v-model="newTodoText"
            >
            <button>Add</button>
        </form>
        <ul>
            <li
            v-for="(todo) in todos"
            v-bind:key="todo.id"
            >{{todo.title}}</li>
        </ul>
</div>
</template>


<script>
export default {
    data() {
        return{
            newTodoText: '',
            // todos:  [
            //     {
            //         id: 1,
            //         title: 'Do the dishes',
            //     },
            //     {
            //         id: 2,
            //         title: 'Take out the trash',
            //     },
            //     {
            //         id: 3,
            //         title: 'Mow the lawn'
            //     }
            // ]
        }
    },
    props: {
        todos:{
            type: Array,
            required: true,
        },
        addNewTodo: {
            type: Function,
            required: true,
        },
        // newTodoText: {
        //     type: String,
        //     required: true,
        // }
    },
    methods: {
        // addNewTodo() {
        //     this.todos.push({
        //         id: this.nextTodoId++,
        //         title: this.newTodoText
        //     })
        //     this.newTodoText = ''
        // },
    }


}
</script>


<style scoped>



</style>
