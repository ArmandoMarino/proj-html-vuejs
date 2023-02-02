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
    <div id="about" class="text-center container">
        <h1>{{ title }}</h1>
        <h3>{{ text }}</h3>
        <button>Fare component neutro bottone</button>
    </div>
</template>

<style lang="scss" scoped>
@use '../../assets/scss/partials/variables' as*;

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