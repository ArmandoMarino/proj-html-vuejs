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
        <img class="img-fluid" src="../assets/img/author-logo-round.png" alt="logo">
        <nav-bar :lists="navlist"></nav-bar>
    </header>
</template>

<style lang="scss" scoped>
header {
    // height: 150px;
    position: absolute;
    right: 0;
    top: 0;
    left: 0;
    background-size: cover;
    background-color: transparent;
    z-index: 1;

    img {
        height: 150px;
        position: relative;
    }
}
</style>