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
    <section id="more" class="p-5">
        <div class="container">
            <div class="title text-center">
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

<style lang="scss" >
@use '../../assets/scss/partials/variables' as*;

#more {
    font-family: 'Newsreader', serif;

    .title {
        h1 {
            font-weight: 600;
            text-transform: capitalize;
            font-size: 30px;
        }

        p {
            font-weight: 600;
            color: $pm-yellow;
        }
    }

    .my-card {
        width: 30%;
        min-height: 400px;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: end;
        border-bottom-right-radius: 50px;
        // TODO
        background: rgb(255, 255, 255);
        background: linear-gradient(180deg, rgba(255, 255, 255, 1) 0%, rgba(0, 1, 1, 0.5270483193277311) 46%, rgba(0, 0, 0, 1) 100%);

        h2 {
            font-weight: 600;
            text-transform: capitalize;
            font-size: 25px;
            color: white;
        }

        p {
            font-weight: 600;
            color: $pm-yellow;
        }

        hr {
            height: 0;
        }
    }

    .cover {

        width: 50px;
    }
}
</style>