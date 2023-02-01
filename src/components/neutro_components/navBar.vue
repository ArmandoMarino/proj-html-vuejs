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
        <ul>
            <li v-for="list in lists">{{ list }}</li>
        </ul>
    </nav>
</template>

<style lang="scss" scoped>
nav {
    height: 20%;

    ul {
        list-style-type: none;
        display: flex;


        li {
            height: 50%;
            padding: 20px;
            text-transform: capitalize;
        }
    }
}
</style>