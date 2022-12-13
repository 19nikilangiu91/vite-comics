<script>
import AppHeader from './components/AppHeader.vue'
import AppJumbotron from './components/AppJumbotron.vue'
import AppMain from './components/AppMain.vue'
import ListProduct from './components/ListProduct.vue'
import AppFooter from './components/AppFooter.vue'


export default {
  components: {
    AppHeader,
    AppJumbotron,
    ListProduct,
    AppMain,
    AppFooter
  },
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
  <AppHeader :links="menu" />
  <AppJumbotron />
  <ListProduct />
  <AppMain />
  <AppFooter />
</template>

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
