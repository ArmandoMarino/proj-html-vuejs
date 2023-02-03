<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
export default {
  components: {
    AppHeader,
    AppMain,
    AppFooter
  }
}

</script>

<template>
  <app-header></app-header>
  <app-main></app-main>
  <app-footer></app-footer>
</template>

<style lang="scss">
@use './assets/scss/partials/variables' as *;
// font-family: 'Cedarville Cursive', cursive;  HERO CURSIVE
// font-family: 'Newsreader', serif;   PRIMARY FONT

// TODO LOADER WITH DATA 
.loader {
  border: 16px solid #f3f3f3;
  /* Light grey */
  border-top: 16px solid #3498db;
  /* Blue */
  border-radius: 50%;
  width: 120px;
  height: 120px;
  animation: spin 2s linear infinite;
}

@keyframes spin {
  0% {
    transform: rotate(0deg);
  }

  100% {
    transform: rotate(360deg);
  }
}

a {
  text-decoration: none;
  color: $pm-white;

  a:hover {
    color: $pm-yellow;
  }
}
</style>