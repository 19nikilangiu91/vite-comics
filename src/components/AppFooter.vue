<script>
export default {
    name: "AppFooter",
    data() {
        return {
            bgLogo: "./src/assets/img/dc-logo-bg.png",
            loges: [
                {
                    image: "./src/assets/img/footer-facebook.png",
                },
                {
                    image: "./src/assets/img/footer-twitter.png",
                },
                {
                    image: "./src/assets/img/footer-youtube.png",

                },
                {
                    image: "./src/assets/img/footer-pinterest.png",
                },
                {
                    image: "./src/assets/img/footer-periscope.png",
                }
            ],
            dcComics: [
                {
                    url: "#",
                    content: "Characters"
                },
                {
                    url: "#",
                    content: "Comics"
                },
                {
                    url: "#",
                    content: "Movies"
                },
                {
                    url: "#",
                    content: "Tv"
                },
                {
                    url: "#",
                    content: "Games"
                },
                {
                    url: "#",
                    content: "Videos"
                },
                {
                    url: "#",
                    content: "News"
                }
            ],
            dc: [
                {
                    url: "#",
                    content: "Terms Of Use"
                },
                {
                    url: "#",
                    content: "Privacy policy (New)"
                },
                {
                    url: "#",
                    content: "Ad Choices"
                },
                {
                    url: "#",
                    content: "Advertsing"
                },
                {
                    url: "#",
                    content: "Jobs"
                },
                {
                    url: "#",
                    content: "Subscriptions"
                },
                {
                    url: "#",
                    content: "Talent Workshops"
                },
                {
                    url: "#",
                    content: "CPSC Certificates"
                },
                {
                    url: "#",
                    content: "Ratings"
                },
                {
                    url: "#",
                    content: "Shop Help"
                },
                {
                    url: "#",
                    content: "Contact Us"
                }
            ],
            sites: [
                {
                    url: "#",
                    content: "DC"
                },
                {
                    url: "#",
                    content: "MAD Magazine"
                },
                {
                    url: "#",
                    content: "DC Kids"
                },
                {
                    url: "#",
                    content: "DC Universe"
                },
                {
                    url: "#",
                    content: "Dc Power Visa"
                }
            ],
            shop: [
                {
                    url: "#",
                    content: "Shop DC"
                },
                {
                    url: "#",
                    content: "Shop DC Collectibles"
                }
            ],
        }
    }
}

</script>

<template>
    <footer>
        <div class="container-footer">
            <section class="footer-up">
                <div class="lists">
                    <ul>
                        <h3>DC COMICS</h3>
                        <li v-for="(link, index) in dcComics" :key="index">
                            <a :href="link.url">
                                {{ link.content }}
                            </a>
                        </li>
                        <div>
                            <ul class="special-list">
                                <h3>SHOP</h3>
                                <li v-for="(link, index) in shop" :key="index">
                                    <a :href="link.url">
                                        {{ link.content }}
                                    </a>
                                </li>
                            </ul>
                        </div>
                    </ul>
                    <ul>
                        <h3>DC</h3>
                        <li v-for="(link, index) in dc" :key="index">
                            <a :href="link.url">
                                {{ link.content }}
                            </a>
                        </li>
                    </ul>
                    <ul>
                        <h3>SITES</h3>
                        <li v-for="(link, index) in sites" :key="index">
                            <a :href="link.url">
                                {{ link.content }}
                            </a>
                        </li>
                    </ul>
                </div>
                <img :src="bgLogo" alt="image dc logo background" class="bg-logo">
            </section>

            <section class="footer-down">
                <button>SIGN-UP NOW!</button>
                <ul>
                    <h3><strong>FOLLOW US</strong></h3>
                    <li v-for="(logo, index) in loges" :key="index">
                        <img :src="logo.image" :alt="'logo ' + (index)">
                    </li>
                </ul>
            </section>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
footer {
    width: 100%;
    min-height: 100px;
    background-color: #303030;

    .container-footer {
        background-image: url(./src/assets/img/footer-bg.jpg);
        background-repeat: no-repeat;
        background-size: cover;
        width: 100%;
        min-height: 350px;

        .footer-up {
            display: flex;
            width: 85%;
            margin: 0 auto;

            div {
                display: flex;

                ul {
                    list-style-type: none;

                    li,
                    a {
                        text-decoration: none;
                    }
                }

                .special-list {
                    position: relative;
                    right: 40px;
                }
            }

            .bg-logo {
                position: relative;
                left: 170px;
                width: 35%;
            }
        }

        .footer-down {
            display: flex;
            justify-content: space-around;
            align-items: center;
            width: 100%;
            margin: 0 auto;
            padding: 10px 0;
            background-color: #303030;

            button {
                background-color: #303030;
                border: 2px solid #0282f9;
                padding: 10px;
            }

            h3 {
                margin: 20px;
                color: #0b7bf4;
            }

            ul {
                display: flex;
                list-style-type: none;

                li {
                    margin: 10px;
                    color: #797979;
                }
            }
        }
    }
}
</style>