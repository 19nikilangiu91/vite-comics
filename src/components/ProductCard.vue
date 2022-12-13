<script>

export default {
    name: "ProductCard",
    props: ["details"]
}

</script>

<template>
    <!-- Card -->
    <div class="prod-card">
        <img :src="details.thumb" alt="">
        <h3>{{ details.series }}</h3>
    </div>
</template>

<style lang="scss" scoped>
.prod-card {
    margin: 5px;
    width: calc((100% / 6) - 10px);

    // background-color: blue
    img {
        width: 100%;
        height: 250px;
    }

    h3 {
        text-align: center;
        font-size: 15px;
    }
}
</style>