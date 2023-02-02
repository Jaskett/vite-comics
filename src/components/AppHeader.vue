<script>
export default {
    name: "AppHeader",

    data() {
        return {
            logo: "img/dc-logo.png",
            links: [
                {
                    text: "CHARACTERS",
                    url: "#",
                    current: false
                },
                {
                    text: "COMICS",
                    url: "#",
                    current: false
                },
                {
                    text: "MOVIES",
                    url: "#",
                    current: false
                },
                {
                    text: "TV",
                    url: "#",
                    current: false
                },
                {
                    text: "GAMES",
                    url: "#",
                    current: false
                },
                {
                    text: "COLLECTIBLES",
                    url: "#",
                    current: false
                },
                {
                    text: "VIDEOS",
                    url: "#",
                    current: false
                },
                {
                    text: "FANS",
                    url: "#",
                    current: false
                },
                {
                    text: "NEWS",
                    url: "#",
                    current: false
                },
                {
                    text: "SHOP",
                    url: "#",
                    current: false 
                }
            ]
        }
    }
}
</script>

<template>
    <header>
        <div class="container">
            <a href="#">
                <img :src="logo" alt="">
            </a>

            <nav>
                <ul v-for="link in links">
                    <li><a href="#">{{ link.text }}</a></li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<style lang="scss" scoped>
@use "../styles/partials/reset.scss" as *;

header {
    height: 95px;
    padding: 10px 0;

    img {
        height: 80px;
    }
}

.container {
    display: flex;
    justify-content: space-between;
}

ul {
    list-style: none;
}
</style>