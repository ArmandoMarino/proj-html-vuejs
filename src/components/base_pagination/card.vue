<script>
export default {
    name: 'card',
    props: {
        title: String,
        class: String,
        text: String,
        image: String,
        alt: String,
        daily: String,
        author: String,
    },
    computed: {
        imagePath() {
            const path = `../../src/assets/img/main/critics/${this.image}`
            return path
        }
    }

}
</script>


<template>
    <div :class="class" class="my-card">
        <h2>{{ title }}</h2>
        <hr>
        <p>{{ text }}</p>
        <div class="d-flex justify-content-center align-item-center">
            <img :src="imagePath" :alt="alt">
            <p>{{ author }},</p>
            <p>{{ daily }}</p>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.my-card {
    margin: 10px;

    h2 {
        text-transform: capitalize;
    }
}
</style>