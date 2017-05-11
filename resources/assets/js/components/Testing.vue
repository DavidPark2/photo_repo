<template>
    <div class="panel-footer">
        {{testingProps}}
    </div>
</template>

<script>
    export default {
        props: ['testingProps'],
        mounted() {
            console.log('Sup!!!!')
        }
    }
</script>
