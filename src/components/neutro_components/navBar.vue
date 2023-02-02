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
            <li v-for="list in lists"><a href="">{{ list }}</a></li>
        </ul>
    </nav>
</template>

<style lang="scss" scoped>
@use '../../assets/scss/partials/variables' as*;

nav {
    height: 20%;

    ul {
        list-style-type: none;
        display: flex;


        li {
            height: 50%;
            padding: 5px;
            text-transform: capitalize;
            font-weight: 600;
            border-top: 2px solid transparent;

            a {
                text-shadow: 2px 3px 5px rgba(0, 0, 0, 0.5);
                padding: 20px;
            }

            li:hover {
                border-top: 2px solid orange;
            }
        }
    }
}
</style>