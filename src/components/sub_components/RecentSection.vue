<script>
import { recentArticles } from '../../data'
import card from '../neutro_components/card.vue';
import NeutroButton from '../neutro_components/NeutroButton.vue';
export default {
    name: 'recentSection',
    components: {
        card,
        NeutroButton
    },
    data() {
        return {
            recentArticles,
        }
    },
}
</script>

<template>
    <section id="recent" class="p-5">
        <div class="container-fluid">
            <div class="row">
                <!-- TITLE -->
                <div class="col-12">
                    <div class="title d-flex justify-content-between">
                        <div>
                            <h2>Recent Articles</h2>
                            <p>READ THE LAST ENTRIES</p>
                        </div>
                        <div class="d-flex justify-content-center align-items-center">
                            <neutro-button class="button" label="All Articles"></neutro-button>
                        </div>
                    </div>
                </div>
                <!-- CARDS -->
                <div class="col-12 col-md-7">
                    <div class="big-card mb-sm-3">
                        <card :class="'thumb-card'" :title="recentArticles[0].title" :thumbPath="recentArticles[0].img"
                            :text="recentArticles[0].text"></card>
                    </div>
                </div>
                <div class="col-12 col-md-4">
                    <card :class="'thumb-card small-card'" :title="recentArticles[1].title"
                        :thumbPath="recentArticles[1].img" :text="recentArticles[1].text"></card>
                    <card :class="'thumb-card small-card'" :title="recentArticles[2].title"
                        :thumbPath="recentArticles[2].img" :text="recentArticles[2].text"></card>
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../../assets/scss/partials/variables' as *;

.button {
    background-color: $pm-yellow;
    padding: 5px 40px;
}

// CUSTOM CARD CLASSES FOR SECTIONS
// BIG-CARD
#recent {
    background-color: $pm-cream;
    font-family: 'Newsreader', serif;

    .title {
        h2 {
            font-weight: 600;
            font-size: 30px;
        }

        p {
            font-weight: 600;
            color: $pm-green;
        }
    }

    .big-card {
        background-color: white;
        color: black;
        padding: 80px;
        line-height: 30px;
        font-size: 15px;
    }

    // SMALL-CARD
    .small-card {
        background-color: white;
        height: 45%;
        // width: 63%;
        // margin: 0 auto;
        margin-bottom: 20px;
        text-align: center;
        padding: 20px;
    }
}
</style>