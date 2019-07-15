<template>
    <todoItem ref="headerChild" :todos="todos" :addNewTodo="addNewTodo" :newTodoText="newTodoText" ></todoItem>
</template>


<script>
import todoItem from './TodoItem';
export default {
    data() {
        return {
            todos: [
                {
                    id: 1,
                    title: 'Do the dishes',
                },
                {
                    id: 2,
                    title: 'Take out the trash',
                },
                {
                    id: 3,
                    title: 'Mow the lawn'
                }
            ],
            newTodoText: '',
        }
    },
    components: {
        todoItem,
    },
    methods: {
        addNewTodo() {
            this.todos.push({
                id: this.nextTodoId++,
                title: this.$refs.headerChild.newTodoText
            })
            this.newTodoText = ''
        },
    }
    
}
</script>


<style scoped>



</style>
