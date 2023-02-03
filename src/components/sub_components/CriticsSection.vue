<script>
import { criticsArticles } from '../../data'
import BaseCard from '../neutro_components/BaseCard.vue';
import NeutroButton from '../neutro_components/NeutroButton.vue';
export default {
    name: 'critics',
    components: {
        BaseCard,
        NeutroButton
    },
    data() {
        return {
            criticsArticles,
        }
    },
}
</script>

<template>
    <section id="critics" class="p-4">
        <!-- TITLE -->
        <div class="container-fluid">
            <div class="row">
                <div class="col-12">
                    <div class="title d-flex justify-content-between">
                        <div>
                            <h2>What the Critics Say</h2>
                            <p>TESTIMONIALS FROM AROUND THE WORLD</p>
                        </div>
                        <div class="d-flex justify-content-center align-items-center">
                            <neutro-button class="button" label="Read All Testimonials"></neutro-button>
                        </div>
                    </div>
                </div>
            </div>
        </div>


        <!-- CARDS -->
        <div class="container-fluid">
            <div class="row">
                <!-- BIG-CARD -->
                <div class="col-12 col-md-7">
                    <base-card :class="'big-card p-3'" :title="criticsArticles[0].title" :text="criticsArticles[0].text"
                        :image="criticsArticles[0].img" :alt="criticsArticles[0].title"
                        :daily="criticsArticles[0].daily" :author="criticsArticles[0].author">
                    </base-card>
                </div>
                <!-- SMALL-CARD -->
                <div class="col-12 col-md-5 mt-sm-4">
                    <base-card :class2="'bg-white'" :class="'small-card'" :title="criticsArticles[1].title"
                        :text="criticsArticles[1].text" :image="criticsArticles[1].img" :alt="criticsArticles[1].title"
                        :daily="criticsArticles[1].daily" :author="criticsArticles[1].author">
                    </base-card>
                    <base-card :class2="'bg-white'" :class="'small-card'" :title="criticsArticles[2].title"
                        :text="criticsArticles[2].text" :image="criticsArticles[2].img" :alt="criticsArticles[2].title"
                        :daily="criticsArticles[2].daily" :author="criticsArticles[2].author">
                    </base-card>
                </div>
            </div>
        </div>
    </section>

</template>

<style lang="scss" scoped>
@use '../../assets/scss/partials/variables' as *;

.button {
    background-color: $pm-yellow;
}

#critics {
    margin-top: 70px;
    margin-bottom: 70px;


    .title {
        font-family: 'Newsreader', serif;
        margin-left: 75px;
        margin-right: 75px;

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
        font-family: 'Newsreader', serif;
        background-image: url(../../assets/img/testimonial2-2x.jpg);
        background-position: center;
        background-size: cover;
        height: 100%;
        border-bottom-right-radius: 100px;
        color: white;
        display: flex;
        flex-direction: column;
        justify-content: center;
        padding: 80px;
        line-height: 30px;

    }

    // SMALL-CARD
    .small-card {
        font-family: 'Newsreader', serif;
        background-color: $pm-cream;
        margin-bottom: 20px;
        text-align: center;
        padding: 20px;
    }

}
</style>