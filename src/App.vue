<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import BlueSection from './components/BlueSection.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  name: "App",
  components: {
    AppHeader,
    AppMain,
    BlueSection,
    AppFooter
  }
}
</script>

<template>
  <AppHeader />
  <AppMain />
  <BlueSection />
  <AppFooter />
</template>

<style lang="scss">
@use "./styles/partials/reset.scss" as *;
@use "./styles/main.scss" as *;
</style>
