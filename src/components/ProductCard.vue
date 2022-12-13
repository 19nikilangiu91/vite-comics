<script>

export default {
    name: "ProductCard",
    promps: ["details"]
}

</script>

<template>
    <!-- Card -->
    <div class="prod-card">
        <img :src="details" alt="">
        <h3>{{ details }}</h3>
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
}
</style>