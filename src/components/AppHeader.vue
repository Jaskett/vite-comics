<script>
export default {
    name: "AppHeader",

    data() {
        return {
            logo: "src/assets/img/dc-logo.png",
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
            <!-- Logo -->
            <a href="#" class="logo">
                <img :src="logo" alt="Logo">
            </a>

            <!-- Nav Bar -->
            <nav>
                <ul>
                    <li v-for="(link, index) in links" :key="index">
                        <a href="link.url" :class="{active: link.current}">{{ link.text }}</a>
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<style lang="scss" scoped>
@use "../styles/partials/reset.scss" as *;
@use "../styles/partials/mixins.scss" as *;

header {
    height: 95px;
    line-height: 95px;

    .container {
        height: 100%;
        @include flex ($type: 'both');

        .logo {
            display: flex;
        }

        .logo img {
            height: 65px;
            line-height: 95px;
        }

        nav ul {
            display: flex;

            li {
                font-size: $font-medium;
                padding-inline: 15px;

                &:hover,
                &.active {
                    border-bottom: 6px solid $primary;
                }

                a {
                    color: $text-nav;
                }
            }
        }
    }
}
</style>