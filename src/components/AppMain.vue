<script>
export default {
    name: "AppMain",
    data() {
        return {
            cards: [
                {
                    image: "/img/buy-comics-digital-comics.png",
                    content: "DIGITAL COMICS",

                },
                {
                    image: "/img/buy-comics-merchandise.png",
                    content: "DC MERCHANDISE",
                },
                {
                    image: "/img/buy-comics-subscriptions.png",
                    content: "SUBSCRPTION",

                },
                {
                    image: "/img/buy-comics-shop-locator.png",
                    content: "COMIC SHOP LOCATOR",

                },
                {
                    image: "/img/buy-dc-power-visa.svg",
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
            <section class="main-loges">
                <!-- Creo un v-for per le "card" richiamando l'array "cards" -->
                <div v-for="(card, index) in cards" :key="index" class="card">
                    <img :src="card.image" :alt="card.image">
                    <h6>{{ card.content }}</h6>
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
            width: 80%;
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