<script>
import { eventsArticles } from '../../data'
import BaseCard from '../neutro_components/BaseCard.vue';
export default {
    name: 'EventsSection',
    components: {
        BaseCard
    },
    data() {
        return {
            eventsArticles
        }
    },
}
</script>

<template>
    <section id="events" class="p-5">
        <div class="container-fluid">
            <div class="row">
                <div class="col-12">
                    <!-- TITLE -->
                    <div class="title text-center">
                        <div>
                            <h1>Upcoming Events</h1>
                            <p>MEET THE AUTHOR IN PERSON</p>
                        </div>
                    </div>
                </div>
                <!-- CARDS -->
                <div v-for="eventsArticle in eventsArticles" class="col-12 col-md-6 col-lg-4 d-flex">
                    <base-card :class="'thumb-card'" :title="eventsArticle.title" :thumbPath="eventsArticle.img"
                        :text="eventsArticle.text"></base-card>
                </div>
            </div>


            <div class="d-flex">

            </div>

        </div>


    </section>

</template>

<style lang="scss" scoped>
@use '../../assets/scss/partials/variables' as *;

#events {
    background-color: $pm-cream;
    font-family: 'Newsreader', serif;

    .title {
        h1 {
            font-size: 30px;
            font-weight: 600;
        }

        p {
            color: $pm-yellow;
            font-weight: 600;
        }
    }
}

.thumb-card {
    display: flex;
    flex-direction: column;
    padding: 20px;
    background-color: white;
    margin: 20px;
    text-align: center;
}
</style>