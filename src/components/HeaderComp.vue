<template>
    <h1 v-text="header"></h1>
</template>

<script>

export default {
    name: "HeaderComp",
    props: ['header'],
    components: {

    }
}
</script>

<style scoped>
h1{
    color: #fff;
}
</style>