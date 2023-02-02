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
nav {
    height: 20%;

    ul {
        list-style-type: none;
        display: flex;


        li {
            height: 50%;
            margin-top: 5px;
            padding: 5px;
            text-transform: capitalize;
            font-weight: 600;

            a {
                text-shadow: 2px 3px 5px rgba(0, 0, 0, 0.5);
                padding: 20px;

            }
        }
    }
}
</style>