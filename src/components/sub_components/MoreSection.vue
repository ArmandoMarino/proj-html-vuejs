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
            moreArticles,
            urlBackground: '/src/assets/img/'
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
            <div class="d-flex justify-content-between">
                <card v-for="moreArticle in moreArticles" :title="moreArticle.title" :text="moreArticle.text"
                    :style="{ backgroundImage: 'url(' + this.urlBackground + moreArticle.img + ')' }"></card>
            </div>

        </div>


    </section>
</template>

<style lang="scss" scoped>
#more {

    .my-card {
        width: 30%;
        min-height: 400px;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: end;
        border-bottom-right-radius: 50px;

        hr {
            height: 0;
        }
    }

    .cover {

        width: 50px;
    }
}
</style>