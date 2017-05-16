<template>
    <div>
        <div class="panel panel-default" v-for="todoData in todoDatas">
            <div class="panel-body">
                {{todoData}}
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        props: ['todoDatas']
    }
</script>