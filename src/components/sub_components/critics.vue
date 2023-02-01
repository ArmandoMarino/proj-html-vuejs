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
    },
}
</script>

<template>
    <div class="say d-flex container">
        <div>
            <h1>What th Critics Say</h1>
            <p>TESTIMONIALS FROM AROUND THE WORLD</p>
        </div>
        <button>CIAO</button>
    </div>
    <!-- CARDS -->
    <div class="container d-flex">
        <div class="left d-flex justify-content-center align-items-center">
            <card :class="'big-card'" :title="criticsArticles[0].title" :text="criticsArticles[0].text"
                :image="criticsArticles[0].img" :alt="criticsArticles[0].title" :daily="criticsArticles[0].daily"
                :author="criticsArticles[0].author">
            </card>
        </div>
        <div class="right">
            <card :class2="'bg-white'" :class="'small-card'" :title="criticsArticles[1].title"
                :text="criticsArticles[1].text" :image="criticsArticles[1].img" :alt="criticsArticles[1].title"
                :daily="criticsArticles[1].daily" :author="criticsArticles[1].author">
            </card>
            <card :class2="'bg-white'" :class="'small-card'" :title="criticsArticles[2].title"
                :text="criticsArticles[2].text" :image="criticsArticles[2].img" :alt="criticsArticles[2].title"
                :daily="criticsArticles[2].daily" :author="criticsArticles[2].author">
            </card>

        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../../assets/scss/partials/variables' as *;

// CUSTOM CARD CLASSES FOR SECTIONS
// BIG-CARD
.big-card {
    background-image: url(../../assets/img/main/critics/testimonial2-2x.jpg);
    background-position: center;
    background-size: cover;
    height: 100%;
    width: 80%;
    border: 1px solid transparent;
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
    background-color: $pm-cream;
    margin: 0 auto;

    width: 80%;
    margin-bottom: 20px;
    text-align: center;
    padding: 20px;
}


// GENERICS
.left {
    flex-basis: 60%;
}

.right {
    flex-basis: 40%;
}
</style>