<script>
export default {
    name: "AppHeader",
    props: {
        links: Array,
    }
    // data() {
    //     return {
    //         logo: "./src/assets/img/dc-logo.png",
    //         links: [
    //             {
    //                 text: "CHARACTERS",
    //                 url: "#",
    //                 current: "true",
    //             },
    //             {
    //                 text: "COMICS",
    //                 url: "#",
    //                 current: "false",
    //             },
    //             {
    //                 text: "MOVIES",
    //                 url: "#",
    //                 current: "false",
    //             },
    //             {
    //                 text: "TV",
    //                 url: "#",
    //                 current: "false",
    //             },
    //             {
    //                 text: "GAMES",
    //                 url: "#",
    //                 current: "false",
    //             },
    //             {
    //                 text: "COLLECTIBLES",
    //                 url: "#",
    //                 current: "false",
    //             },
    //             {
    //                 text: "VIDEOS",
    //                 url: "#",
    //                 current: "false",
    //             },
    //             {
    //                 text: "FANS",
    //                 url: "#",
    //                 current: "false",
    //             },
    //             {
    //                 text: "NEWS",
    //                 url: "#",
    //                 current: "false",
    //             },
    //             {
    //                 text: "SHOP",
    //                 url: "#",
    //                 current: "false",
    //             }
    //         ]
    //     }
    // }
}

</script>

<template>
    <header>
        <div class="container">
            <nav>
                <div class="logo">
                    <a href="#">
                        <img src="/src/assets/img/dc-logo.png" alt="logo">
                    </a>
                </div>
                <ul>
                    <li v-for="(link, index) in links" :key="index">
                        <a :class="{ active: links.current }" :href="link.url">
                            {{ link.text }}
                        </a>
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<style lang="scss" scoped>
header {
    width: 100%;
    background-color: white;

    .container {
        width: 80%;
        margin: 0 auto;

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;

            .logo {
                width: 50%;
                padding: 10px;
            }

            ul {
                display: flex;
                list-style: none;

                li a {
                    text-decoration: none;
                    margin-left: 15px;
                    padding-bottom: 50px;


                    &.active,
                    &:hover {
                        color: #0282f9;
                        border-bottom: 10px solid #0282f9;
                    }
                }
            }
        }
    }
}
</style>