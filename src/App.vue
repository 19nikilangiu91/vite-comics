<script>
// Importo i "components"
import AppHeader from './components/AppHeader.vue'
import AppJumbotron from './components/AppJumbotron.vue'
import AppMain from './components/AppMain.vue'
import ListProduct from './components/ListProduct.vue'
import AppFooter from './components/AppFooter.vue'


export default {
  // Esporto i "components"
  components: {
    AppHeader,
    AppJumbotron,
    ListProduct,
    AppMain,
    AppFooter
  },

  // Esporto i data da "AppHeader" per collegare la "Nav" con "Ul" di "AppFooter"
  data() {
    return {

      menu: [
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
  <!-- Richiamo i "components" -->
  <!-- Collego l'array "links" dicendo che è uguale a "menu" che sarebbe l'array in data -->
  <AppHeader :links="menu" />
  <AppJumbotron />
  <ListProduct />
  <AppMain />
  <AppFooter />
</template>

<!-- Inserisco i due "@use" e "lang='scss'" -->
<style lang="scss">
@use './styles/partials/variables' as*;
@use './styles/partials/general.scss' as*;

li,
a {
  color: $primary;
}

li,
h3,
h6,
button {
  color: $secondary;
}
</style>
