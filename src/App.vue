<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
export default {
  components: {
    AppHeader,
    AppMain
  }
}
</script>

<template>
  <app-header></app-header>
  <app-main></app-main>
</template>

<style lang="scss">
@use './assets/scss/partials/variables' as *;
// font-family: 'Cedarville Cursive', cursive;  HERO CURSIVE
// font-family: 'Newsreader', serif;   PRIMARY FONT


a {
  text-decoration: none;
  color: white;

  a:hover {
    color: $pm-yellow;
  }
}
</style>