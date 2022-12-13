<script>
export default {
    name: "AppMain",
    data() {
        return {
            jumbotron: "/img/jumbotron.jpg",
        }
    }
}

</script>

<template>
    <main>
        <div class="container-main">
            <section class="main-content">
                <div>
                    <img :src="jumbotron" :alt="jumbotron" class="jumbotron">
                </div>
            </section>
        </div>
    </main>
</template>

<style lang="scss" scoped>
main {
    width: 100%;


    .container-main {
        width: 100%;
        margin: 0 auto;
        background-color: #1c1c1c;

        .main-content {
            width: 100%;

            .jumbotron {
                width: 100%;
                height: 500px;
                background-size: cover;
            }
        }
    }
}
</style>