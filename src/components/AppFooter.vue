<script>
export default {
    name: "AppFooter",
    data() {
        return {
            comics: [
                "Characters",
                "Comics",
                "Movies",
                "TV",
                "Games",
                "Videos",
                "News"
            ],
            shops: [
                "Shop DC",
                "Shop DC Collectibles"
            ],
            DC: [
                "Terme of Use",
                "Privacy Policy (New)",
                "Ad Choices",
                "Advertising",
                "Jobs",
                "Subscriptions",
                "Talent Workshop",
                "CPCS Certificates",
                "Ratings",
                "Shop Help",
                "Contact us"
            ],
            sites: [
                "DC",
                "MAD Magazine",
                "DC Kids",
                "DC Universe",
                "DC Power Visa"
            ],
            socials: [
                "src/assets/img/footer-facebook.png",
                "src/assets/img/footer-twitter.png",
                "src/assets/img/footer-youtube.png",
                "src/assets/img/footer-pinterest.png",
                "src/assets/img/footer-periscope.png"
            ]
        }
    }
}
</script>

<template>
    <footer>
        <!-- Section 1 -->
        <section class="links">
            <div class="container">
                <div class="cols">
                    <!-- Colonna Sx -->
                    <div class="col">
                        <h3>DC COMICS</h3>

                        <ul>
                            <li v-for="comic in comics">
                                <a href="#">{{ comic }}</a>
                            </li>
                        </ul>

                        <h3 class="mt-top">SHOP</h3>

                        <ul>
                            <li v-for="shop in shops">
                                <a href="#">{{ shop }}</a>
                            </li>
                        </ul>
                    </div>

                    <!-- Colonna Centrale -->
                    <div class="col center">
                        <h3>DC</h3>

                        <ul>
                            <li v-for="link in DC">
                                <a href="#">{{ link }}</a>
                            </li>
                        </ul>
                    </div>

                    <!-- Colonna Dx -->
                    <div class="col">
                        <h3>SITES</h3>

                        <ul>
                            <li v-for="site in sites">
                                <a href="#">{{ site }}</a>
                            </li>
                        </ul>
                    </div>
                </div>

                <div class="bg-logo">
                    <img src="../assets/img/dc-logo-bg.png" alt="">
                </div>
            </div>
        </section>

        <!-- Section 2 -->
        <section class="sub-footer">
            <div class="container">
                
                <!-- Button -->
                <a class="sign-up">SIGN-UP NOW!</a>
                
                <!-- Social -->
                <div class="social">
                    <span>FOLLOW US</span>
                    <ul>
                        <li v-for="social in socials">
                            <img :src="social" alt="Social">
                        </li>
                    </ul>
                </div>
            </div>
        </section>
    </footer>
</template>

<style lang="scss" scoped>
@use "../styles/partials/reset.scss" as *;
@use "../styles/partials/mixins.scss" as *;

footer {
    // Section 1
    .links {
        background-image: url(../assets/img/footer-bg.jpg);
        background-size: cover;
        color: $text-white;

        .container {
            @include flex ($type: 'both');
            position: relative;
            overflow: hidden;

            .cols {
                display: flex;

                .col {
                    padding: 30px 0;

                    .mt-top {
                        margin-top: 20px;
                    }

                    a {
                        color: #5f5f5f;
                        font-size: $font-small;
                    }

                    &.center {
                        padding-inline: 30px;
                    }
                }
            }

            .bg-logo {
                width: 500px;
                height: 350px;
            }

            .bg-logo img {
                position: absolute;
                right: 0;
                top: -80px;
            }
        }
    }

    // Section 2
    .sub-footer {
        height: 90px;
        background-color: #303030;

        .container {
            @include flex ($type: 'both');
            height: 100%;

            .sign-up {
                color: $text-white;
                padding: 10px;
                border: 2px solid $primary;
            }

            .social {
                @include flex ($type: 'center');

                ul {
                    @include flex ($type: 'center');

                    li {
                        padding: 0 10px;
                    }
                }

                span {
                    color: $primary;
                }
            }
        }
    }
}
</style>