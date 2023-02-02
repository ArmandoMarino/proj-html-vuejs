<script>
import { eventsArticles } from '../../data'
import card from '../neutro_components/card.vue';
export default {
    name: 'EventsSection',
    components: {
        card
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
        <div class="container">
            <!-- TITLE -->
            <div class="title text-center">
                <div>
                    <h1>Upcoming Events</h1>
                    <p>MEET THE AUTHOR IN PERSON</p>
                </div>
            </div>
            <!-- CARDS -->
            <div class="d-flex">
                <card v-for="eventsArticle in eventsArticles" :class="'thumb-card'" :title="eventsArticle.title"
                    :thumbPath="eventsArticle.img" :text="eventsArticle.text"></card>
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