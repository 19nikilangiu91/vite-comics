<script>
export default {
    name: "AppHeader",
    data() {
        return {
            links: [
                {
                    text: "CHARACTERS",
                    url: "#",
                    current: "true",
                },
                {
                    text: "COMICS",
                    url: "#",
                    current: "false",
                },
                {
                    text: "MOVIES",
                    url: "#",
                    current: "false",
                },
                {
                    text: "TV",
                    url: "#",
                    current: "false",
                },
                {
                    text: "GAMES",
                    url: "#",
                    current: "false",
                },
                {
                    text: "COLLECTIBLES",
                    url: "#",
                    current: "false",
                },
                {
                    text: "VIDEOS",
                    url: "#",
                    current: "false",
                },
                {
                    text: "FANS",
                    url: "#",
                    current: "false",
                },
                {
                    text: "NEWS",
                    url: "#",
                    current: "false",
                },
                {
                    text: "SHOP",
                    url: "#",
                    current: "false",
                }
            ]
        }
    }
}

</script>

<template>
    <header>
        <nav>
            <div class="logo">
                <a href="#">
                    <img src="../assets/img/dc-logo.png" alt="Dc-logo">
                </a>
            </div>
            <li v-for="(link, index) in links" :key="index">
                <a :href="link.url">
                    {{ link.text }}
                </a>
            </li>
        </nav>
    </header>
</template>

<style lang="scss" scoped>
header {
    margin: 0 auto;
    width: 80%;

    nav {
        display: flex;
        justify-content: space-between;
        align-items: center;

        .logo {
            width: 50%;
        }

        li,
        a {
            list-style-type: none;
            text-decoration: none;
            margin: 3px;
        }
    }
}
</style>