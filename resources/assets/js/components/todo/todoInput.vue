<template>
    <div>
        <div class="form-group">
            <input class="form-control" type="text" v-model="newInput">
        </div>
        <div class="form-group">
            <button class="btn btn-primary" @click="addTodo">Click Me!</button>
        </div>
    </div>
</template>

<script>
    export default {
        data: function () {
            return {
                newInput: ''
            }
        },
        methods: {
            addTodo: function () {
                this.$emit('new-todo', this.newInput)
                this.newInput = '';
            }
        }
    }
</script>