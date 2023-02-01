<script>
import { navlist } from '../data/index.js'
import navBar from './neutro_components/navBar.vue';
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
    <header class="d-flex justify-content-between">
        <img class="img-fluid" src="../assets/img/header/author-logo-round.png" alt="logo">
        <nav-bar :lists="navlist"></nav-bar>
    </header>
</template>

<style lang="scss" scoped>
header {
    height: 150px;
    background-size: cover;
    background-color: transparent;

    img {
        height: 150px;
    }
}
</style>