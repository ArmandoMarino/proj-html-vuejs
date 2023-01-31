<script>
import AppHero from './AppHero.vue';
import about from './sub_components/about.vue';
export default {
    name: 'AppMain',
    components: {
        AppHero,
        about
    },
    data() {
        return {
            about:
            {
                "title": 'more about damon vaughn',
                "text": 'Damon Vaughn is a professor of psychology at the University of Toronto, a clinical psychologis and the author of the multi- milion copy bestseller "The Story of my life."'
            }
        }
    }
}
</script>

<template>
    <main>
        <app-hero></app-hero>
        <about :title="this.about.title" :text="this.about.text"></about>
    </main>
</template>

<style>

</style>