<script>
export default {
    name: 'card',

    props: {
        title: String,
        class: String,
        class2: String,
        class3: String,
        text: String,
        image: String,
        thumbPath: String,
        alt: String,
        daily: String,
        author: String,
    },
    computed: {
        // ICON-PATH GENERATOR
        iconPath() {
            const path = `../../src/assets/img/${this.image}`
            return path
        },
        // IMAGE THUMB PATH GENERATOR
        imagePath() {
            const path = `../../src/assets/img/${this.thumbPath}`
            return path
        },

    }


}
</script>


<template>
    <div :class="class" class="my-card">
        <!-- IF thumbPath exist RENDER THUMBIMAGE -->
        <div class="thumb" v-if="thumbPath"><img class="img-fluid" :class="class3" :src="imagePath" :alt="alt"></div>
        <h2>{{ title }}</h2>
        <hr>
        <p v-if="text">{{ text }}</p>
        <!-- IF author exist RENDER ENTIRE DIV WITH AUTHOR AND DAILY -->
        <div v-if="author" class="b-author d-flex align-item-center" :class="class2">
            <img class="img-fluid" :src="iconPath" :alt="alt">
            <p>{{ author }},</p>
            <p>{{ daily }}</p>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.my-card>* {
    padding: 5px;
}

.thumb {
    img {
        display: inline-block;
    }
}

.b-author {
    background-color: transparent;

    p {
        margin: 0;
        padding: 2px;
        text-align: center;
        line-height: 40px;
        text-transform: capitalize;
    }

    img {
        padding: 5px;
        height: 40px;
    }
}

h2 {
    text-transform: capitalize;
    font-size: 1.3rem;
    font-weight: 600;
}

hr {
    margin: 0;
}
</style>