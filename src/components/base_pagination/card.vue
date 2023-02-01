<script>
export default {
    name: 'card',
    props: {
        title: String,
        class: String,
        text: String,
        image: String,
        thumbPath: String,
        alt: String,
        daily: String,
        author: String,
        class2: String
    },
    computed: {
        // ICON-PATH GENERATOR
        iconPath() {
            const path = `../../src/assets/img/main/critics/${this.image}`
            return path
        },
        // IMAGE THUMB PATH GENERATOR
        imagePath() {
            const path = `../../src/assets/img/main/upcoming_events/${this.thumbPath}`
            return path
        },

    }


}
</script>


<template>
    <div :class="class" class="my-card">
        <!-- IF thumbPath exist RENDER THUMBIMAGE -->
        <div class="thumb" v-if="thumbPath"><img :src="imagePath" :alt="alt"></div>
        <h2>{{ title }}</h2>
        <span>
            <hr>
        </span>
        <p>{{ text }}</p>
        <!-- IF author exist RENDER ENTIRE DIV WITH AUTHOR AND DAILY -->
        <div v-if="author" class="b-author d-flex align-item-center" :class="class2">
            <img class="img-fluid" :src="iconPath" :alt="alt">
            <p>{{ author }},</p>
            <p>{{ daily }}</p>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.thumb {
    img {
        width: 95%;

    }
}

.b-author {
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
</style>