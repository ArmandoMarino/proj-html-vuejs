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
    <section id="events">
        <div class="container">
            <div class="d-flex">
                <div>
                    <h1>Upcoming Events</h1>
                    <p>MEET THE AUTHOR IN PERSON</p>
                </div>
            </div>
            <!-- CARDS -->
            <div class="d-flex">
                <div class="d-flex">
                    <card v-for="eventsArticle in eventsArticles" :class="'thumb-card'" :title="eventsArticle.title"
                        :thumbPath="eventsArticle.img" :text="eventsArticle.text"></card>
                </div>
            </div>
        </div>


    </section>

</template>

<style lang="scss" scoped>
@use '../../assets/scss/partials/variables' as *;

#events {
    background-color: $pm-cream;
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