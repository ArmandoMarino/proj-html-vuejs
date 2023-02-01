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
        class2: String
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
        <span>
            <hr>
        </span>
        <p>{{ text }}</p>
        <div class="d-flex align-item-center" :class="class2">
            <img class="img-fluid" :src="imagePath" :alt="alt">
            <p>{{ author }},</p>
            <p>{{ daily }}</p>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.my-card {

    div {
        background-color: transparent;

        p {
            margin: 0;
            text-align: center;
            line-height: 40px;
        }

        img {
            padding: 5px;
            height: 40px;
        }
    }

    h2 {
        text-transform: capitalize;
    }
}
</style>