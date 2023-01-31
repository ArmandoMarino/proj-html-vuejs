<script>
export default {
    name: 'navBar',
    props: {
        lists: Array,
        headerLogo: String,
        alt: String
    }
}
</script>

<template>
    <nav>
        <ul class="d-flex">
            <li v-for="list in lists">{{ list }}</li>
        </ul>
    </nav>
</template>

<style lang="scss" scoped>
nav {
    ul {
        list-style-type: none;
    }
}
</style>