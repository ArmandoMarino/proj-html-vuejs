<script>
export default {
    name: 'about',
    props: {
        title: String,
        text: String
    }
}
</script>

<template>
    <div id="about" class="text-center d-flex">
        <h1>{{ title }}</h1>
        <h3>{{ text }}</h3>
    </div>
</template>

<style lang="scss" scoped>

</style>