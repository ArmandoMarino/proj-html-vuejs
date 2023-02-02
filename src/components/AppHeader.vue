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
    <header>
        <div class="">
            <div class="row">
                <div class="col-3">
                    <img class="img-fluid" src="../assets/img/author-logo-round.png" alt="logo">
                </div>
                <div class="col-8">
                    <nav-bar :lists="navlist"></nav-bar>
                </div>
            </div>
        </div>

    </header>
</template>

<style lang="scss" scoped>
header {
    position: absolute;
    right: 0;
    left: 0;
    background-size: cover;
    background-color: transparent;
    z-index: 1;

    img {
        max-height: 150px;
        position: relative;
    }
}
</style>