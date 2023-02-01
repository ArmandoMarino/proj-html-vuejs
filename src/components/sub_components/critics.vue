<script>
import { criticsArticles } from '../../data'
import card from '../base_pagination/card.vue';
export default {
    name: 'critics',
    components: {
        card
    },
    data() {
        return {
            criticsArticles
        }
    }
}
</script>

<template>
    <div class="say">
        <div>
            <h1>What th Critics Say</h1>
            <p>TESTIMONIALS FROM AROUND THE WORLD</p>
        </div>
        <button>CIAO</button>
    </div>
    <!-- CARDS -->
    <div class="container d-flex">
        <div class="left">
            <card :title="criticsArticles[0].title" :text="criticsArticles[0].text"></card>
        </div>
        <div class="right">
            <card :title="criticsArticles[1].title" :text="criticsArticles[1].text"></card>
            <card :title="criticsArticles[2].title" :text="criticsArticles[2].text"></card>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.left {
    flex-basis: 60%;
}

.right {
    flex-basis: 40%;
}
</style>