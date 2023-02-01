<script>
import { moreArticles } from '../../data'

import card from '../neutro_components/card.vue';
export default {
    name: 'MoreSection',
    components: {
        card
    },
    data() {
        return {
            moreArticles
        }
    },
}
</script>

<template>
    <section id="more">
        <div class="container">
            <div class="d-flex">
                <div>
                    <h1>dig a little deeper into damon vaughn</h1>
                    <p>FIND OUT MORE ABOUT THE AUTHOR HIMSELF</p>
                </div>
            </div>
            <!-- CARDS -->
            <div class="d-flex">
                <div class="d-flex">
                    <card v-for="moreArticle in moreArticles" :class="'thumb-card'" :title="moreArticle.title"
                        :thumbPath="moreArticle.img" :text="moreArticle.text"></card>
                </div>
            </div>
        </div>


    </section>
</template>

<style>

</style>