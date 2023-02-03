<script>
import { moreArticles } from '../../data'

import BaseCard from '../neutro_components/BaseCard.vue';
export default {
    name: 'MoreSection',
    components: {
        BaseCard
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
    <section id="more" class="m-3">
        <div class="container-fluid">
            <div class="row">
                <!-- TITLE -->
                <div class="col-12">
                    <div class="title text-center">
                        <div>
                            <h1>dig a little deeper into damon vaughn</h1>
                            <p>FIND OUT MORE ABOUT THE AUTHOR HIMSELF</p>
                        </div>
                    </div>
                </div>
                <!-- CARDS -->
                <div v-for="moreArticle in moreArticles" class="col-12 col-md-4 mt-3 ">
                    <base-card :title="moreArticle.title" :text="moreArticle.text"
                        :style="{ backgroundImage: 'url(' + this.urlBackground + moreArticle.img + ')' }"></base-card>
                </div>
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
        text-shadow: 2px 3px 5px rgba(0, 0, 0, 0.5);
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