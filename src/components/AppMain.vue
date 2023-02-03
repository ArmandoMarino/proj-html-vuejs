<script>
import AppHero from '../components/sub_components/AppHero.vue';
import AboutSection from './sub_components/AboutSection.vue';
import AudioBook from './sub_components/AudioBook.vue';
import CriticsSection from './sub_components/CriticsSection.vue';
import EventsSection from './sub_components/EventsSection.vue';
import SubscribeSection from './sub_components/SubscribeSection.vue';
import MoreSection from './sub_components/MoreSection.vue';
import RecentSection from './sub_components/RecentSection.vue';
export default {
    name: 'AppMain',
    components: {
        AppHero,
        AboutSection,
        AudioBook,
        CriticsSection,
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
        <about-section :title="this.about.title" :text="this.about.text"></about-section>
        <audio-book></audio-book>
        <critics-section></critics-section>
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