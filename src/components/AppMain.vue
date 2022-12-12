<script>
export default {
    name: "AppMain",
}

</script>

<template>
    <main>
        <div class="container-main">
            <section class="main-content">
                <h1>Add Content</h1>
            </section>

            <section class="main-loges"></section>

        </div>
    </main>
</template>

<style lang="scss" scoped>
main {
    width: 100%;
    // DEBUG
    background-color: red;

    .container-main {
        width: 80%;
        margin: 0 auto;
        // DEBUG
        background-color: yellow;
    }
}
</style>