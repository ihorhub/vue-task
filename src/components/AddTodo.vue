<template>
    <div>
        <h1>AddTodo</h1>
        <input type="text" v-model="text">
        {{text}}
        <button @click="addtext">ADD</button>

    </div>

</template>

<script>

    export default {
        name: 'AddTodo',

        data() {
            return {
                text: ''
            }
        },
        methods: {
            addtext() {
                this.$emit('pushText', this.text)

            }
        }
    }

</script>

<style>

</style>
