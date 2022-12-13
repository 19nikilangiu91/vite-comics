<script>
import { objectToString } from '@vue/shared';


export default {
    name: "ProductCard",
    // Creo il props per passare i dati da "ProductCard" a "ListProduct" richiamando ":details" che mi passera il "product".
    // Possiamo scriverlo in entrambi i modi.
    // props: ["details"]
    props: {
        details: Object
    }
}

</script>

<template>
    <!-- Card -->
    <div class="prod-card">
        <!-- Richiamo tramite il props "details" il "thumb" dall'array "products" -->
        <img :src="details.thumb" :alt="details.series">
        <!-- Richiamo tramite il props "details" la "series" dall'array "products" -->
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