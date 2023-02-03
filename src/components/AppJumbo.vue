<script>
export default {
    name: "AppJumbo",
    data() {
        return {
            jumbo: "src/assets/img/jumbotron.jpg"
        }
    }
}
</script>

<template>
    <section>
        <img :src="jumbo" alt="">
    </section>
</template>

<style lang="scss" scoped>
@use "../styles/partials/reset.scss" as *;

section img {
    object-fit: cover;
    object-position: 20% 0;
    height: 400px;
    width: 100%;
}
</style>