<script>
import { recentArticles } from '../../data'
import card from '../neutro_components/card.vue';
export default {
    name: 'recentSection',
    components: {
        card
    },
    data() {
        return {
            recentArticles,
        }
    },
}
</script>

<template>
    <section id="recent">
        <div class="container">
            <div class="d-flex">
                <div>
                    <h1>What th Critics Say</h1>
                    <p>TESTIMONIALS FROM AROUND THE WORLD</p>
                </div>
                <button>CIAO</button>
            </div>
            <!-- CARDS -->
            <div class="d-flex">
                <div class="left d-flex justify-content-center">
                    <div class="big-card">
                        <card :class="'thumb-card'" :title="recentArticles[0].title" :thumbPath="recentArticles[0].img"
                            :text="recentArticles[0].text"></card>
                    </div>

                </div>
                <div class="right d-flex flex-column justify-content-between align-items-center">
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

// CUSTOM CARD CLASSES FOR SECTIONS
// BIG-CARD
#recent {
    background-color: $pm-cream;

    .big-card {
        height: 95%;
        background-color: white;
        color: black;
        display: flex;
        flex-direction: column;
        justify-content: center;
        padding: 80px;
        line-height: 30px;
        font-size: 15px;
    }

    // SMALL-CARD
    .small-card {
        background-color: white;
        height: 98%;
        width: 66%;
        margin-bottom: 20px;
        text-align: center;
        padding: 20px;
    }


    // GENERICS
    .left {
        flex-basis: 70%;
        height: 150%;
    }

    .right {
        flex-basis: 40%;
        height: 70%;
    }




}
</style>