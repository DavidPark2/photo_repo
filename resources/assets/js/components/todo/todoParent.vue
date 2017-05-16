<template>
    <div class="container">
        <div class="row">
            <todo-input v-on:new-todo="newTodo"></todo-input>
            <todo-cards
                :todo-datas=todoDatas></todo-cards>
        </div>
    </div>
</template>

<script>
    export default {
        components: {
            todoInput: require('./todoInput.vue'),
            todoCards: require('./todoCards.vue')
        },
        mounted() {
            console.log('yay! Vues working!')
        },
        data: function () {
            return {
                todoDatas: ['First Todo Item!', 'Second']
            }
        },
        methods: {
            newTodo: function (data) {
                this.todoDatas.push(data)
            }
        },
        getTodo() {
            axios.get('api/todo')
                .then(response => {
                    this.todoDatas = response.data
                })
                .catch(e => {
                    this.errors.push(e)
                })
        }
    }
</script>