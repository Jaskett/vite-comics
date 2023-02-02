<script>
import AppHeader from './components/AppHeader.vue';

export default {
  name: "App",
  components: {
    AppHeader
  }
}
</script>

<template>
  <AppHeader />
</template>

<style lang="scss" scoped>
@use "./styles/partials/reset.scss" as *;
@use "./styles/main.scss" as *;
</style>
