<script>
export default {
    name: "AppFooter",
    data() {
        return {
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
            ]
        }
    }
}

</script>

<template>
    <footer>
        <div class="container-footer">
            <section class="footer-up">
                <button>SIGN-UP NOW!</button>
            </section>

            <section class="footer-down">
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
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 80%;
        margin: 0 auto;

        .footer-up {
            button {
                background-color: #303030;
                border: 2px solid #0282f9;
                padding: 10px;
            }
        }

        .footer-down {
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