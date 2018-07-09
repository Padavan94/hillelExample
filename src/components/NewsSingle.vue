<template>
    <li class="news-single">
        {{item.title}}
    </li>
</template>

<script>
    export default {
        name: "news-single",
        props: ['item']
    }
</script>

<style scoped>

</style>