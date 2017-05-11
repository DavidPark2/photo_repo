<template>
    <div class="container">
        <div class="row">
            <div class="col-md-8 col-md-offset-2">
                <div class="panel panel-default">
                    <div class="panel-heading">Example Component</div>

                    <div class="panel-body">
                        I'm an example component!
                    </div>
                    <testing
                        v-bind:testing-props=counter></testing>
                </div>
                <button @click="increase">Increase</button>
                <button @click="decrease">Decrease</button>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        components: {
            testing: require('./Testing.vue')
        },
        mounted() {
            console.log('Component mounted.')
        },
        data: function () {
            return {
                counter: 1
            }
        },
        methods: {
            increase: function() {
                this.counter++
            },
            decrease: function() {
                this.counter--
            }
        }
    }
</script>
