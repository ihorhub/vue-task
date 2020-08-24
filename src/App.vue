<template>
    <div>
        <h1>MEGA TODO LIST</h1>
        <AddTodo @pushText="pusharr">

        </AddTodo>
        <TodoList :array="arrList"

                  @splicetext="remItem"
        ></TodoList>

    </div>
</template>

<script>

    import AddTodo from "./components/AddTodo";
    import TodoList from "./components/TodoList";
    import TodoItem from "./components/TodoItem";

    export default {
        name: 'App',

        components: {
            AddTodo, TodoList
        },
        data() {
            return {
                arrList: []
            }
        },
        methods: {
            pusharr() {
                this.arrList.push(this.text)
            },
            remItem(event) {
                this.arrList.splice(event, 1)
            }
        }
    }
</script>

<style>

</style>
