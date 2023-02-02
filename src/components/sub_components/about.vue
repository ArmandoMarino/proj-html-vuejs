<script>
import NeutroButton from '../neutro_components/NeutroButton.vue';
export default {
    name: 'about',
    props: {
        title: String,
        text: String,
    },
    components: {
        NeutroButton
    }
}
</script>

<template>
    <div id="about" class="text-center">
        <div class="container">
            <div class="row">
                <div class="col-12">
                    <h1>{{ title }}</h1>
                    <h3>{{ text }}</h3>
                    <neutro-button class="button" label="Meet the Author"></neutro-button>
                </div>
            </div>
        </div>

    </div>
</template>

<style lang="scss" scoped>
@use '../../assets/scss/partials/variables' as*;

.button {
    background-color: $pm-green;
}

#about {
    margin: 50px;

    h1 {
        font-size: 50px;
        text-transform: capitalize;
        font-family: 'Cedarville Cursive', cursive;
        color: $pm-yellow
    }
}

#about>* {
    margin: 20px
}
</style>