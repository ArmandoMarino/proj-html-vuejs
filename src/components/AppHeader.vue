<script>
import { navlist } from '../data/index.js'
import navBar from './base_pagination/navBar.vue';
export default {
    name: 'AppHeader',
    components: {
        navBar,
    },
    data() {
        return {
            navlist
        }
    }
}
</script>

<template>
    <header>
        <img src="../assets/img/header/author-logo-round.png" alt="logo">

        <nav-bar :lists="navlist"></nav-bar>
    </header>
</template>

<style lang="scss" scoped>
header {
    height: 150px;
    background-color: red;
}
</style>