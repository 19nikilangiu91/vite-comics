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
  }
}

</script>

<template>
  <AppHeader />
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
