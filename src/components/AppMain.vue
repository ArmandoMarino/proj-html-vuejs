<script>
import AppHero from './AppHero.vue';
import about from './sub_components/about.vue';
import audioBook from './sub_components/audioBook.vue';
import critics from './sub_components/critics.vue';
import EventsSection from './sub_components/EventsSection.vue';
import SubscribeSection from './sub_components/SubscribeSection.vue';
import MoreSection from './sub_components/MoreSection.vue';
import RecentSection from './sub_components/RecentSection.vue';
export default {
    name: 'AppMain',
    components: {
        AppHero,
        about,
        audioBook,
        critics,
        EventsSection,
        SubscribeSection,
        MoreSection,
        RecentSection
    },
    data() {
        return {
            about:
            {
                "title": 'more about damon vaughn',
                "text": 'Damon Vaughn is a professor of psychology at the University of Toronto, a clinical psychologis and the author of the multi- milion copy bestseller "The Story of my life."'
            },
        }
    }
}
</script>

<template>
    <main>
        <app-hero></app-hero>
        <about :title="this.about.title" :text="this.about.text"></about>
        <audio-book></audio-book>
        <critics></critics>
        <events-section></events-section>
        <subscribe-section></subscribe-section>
        <more-section></more-section>
        <recent-section></recent-section>
    </main>
</template>

<style>
main {
    position: relative;
}
</style>