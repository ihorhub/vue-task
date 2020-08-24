<template>
    <div>
        <h1>TodoList</h1>

        <div v-for="(item,i) in arrList " :key="i">
            {{item}}
            <TodoItem :itemList="item"
                      @deleteItem="dell"
            >

            </TodoItem>
        </div>

        <TodoItem></TodoItem>

    </div>

</template>

<script>






    import TodoItem from "./TodoItem";

    export default {
        name: 'TodoList',
        props: {
            array: {
                type: Array,
                require: true
            }
        },
        comments: {TodoItem},

        method: {
            dell() {
                this.$emit('splicetext', this.item)

            }
        }
    }


</script>

<style>


</style>
