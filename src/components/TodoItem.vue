<template>
    <div>
        <h1>TodoItem</h1>
        <span>

{{itemList}}
        <button @click="remove"> delete </button>

</span>
    </div>

</template>

<script>


    export default {
        name: 'TodoItem',
        props: {
            itemList: {
                type: String,
                require: true
            },
            methods: {
                remove() {
                    this.$emit('deleteItem', this.itemList)
                }

            }
        }
    }

</script>

<style>

</style>
