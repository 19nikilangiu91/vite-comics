<script>
export default {
    name: "AppMain",
    data() {
        return {
            jumbotron: "./src/assets/img/jumbotron.jpg",
            cards: [
                {
                    image: "./src/assets/img/buy-comics-digital-comics.png",
                    content: "DIGITAL COMICS",

                },
                {
                    image: "./src/assets/img/buy-comics-merchandise.png",
                    content: "DC MERCHANDISE",
                },
                {
                    image: "./src/assets/img/buy-comics-subscriptions.png",
                    content: "SUBSCRPTION",

                },
                {
                    image: "./src/assets/img/buy-comics-shop-locator.png",
                    content: "COMIC SHOP LOCATOR",

                },
                {
                    image: "./src/assets/img/buy-dc-power-visa.svg",
                    content: "DC POWER VISA",

                }
            ]
        }
    }
}

</script>

<template>
    <main>
        <div class="container-main">
            <section class="main-content">
                <div>
                    <img :src="jumbotron" alt="jumbotron" class="jumbotron">
                </div>
            </section>

            <section class="main-loges">
                <div v-for="(card, index) in cards" :key="index" class="card">
                    <img :src="card.image" alt="">
                    <h6>{{ card.content }}</h6>
                </div>
            </section>
        </div>
    </main>
</template>

<style lang="scss" scoped>
main {
    width: 100%;
    // DEBUG
    background-color: red;

    .container-main {
        width: 100%;
        margin: 0 auto;
        background-color: #0282f9;

        .main-content {
            width: 100%;

            .jumbotron {
                width: 100%;
                height: 500px;
                background-size: cover;
            }
        }

        .main-loges {
            width: 70%;
            margin: 0 auto;
            display: flex;
            justify-content: center;

            .card {
                display: flex;
                justify-content: center;
                width: 50%;
                height: 50%;
                margin: 10px 0;
            }

            img {
                width: 45px;
                height: 50px;
            }

            h6 {
                margin-left: 10px;
            }
        }
    }
}
</style>