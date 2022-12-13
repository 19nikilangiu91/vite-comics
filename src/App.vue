<script>
import AppHeader from './components/AppHeader.vue'
import AppMain from './components/AppMain.vue'
import ListProduct from './components/ListProduct.vue'
import AppFooter from './components/AppFooter.vue'


export default {
  components: {
    AppHeader,
    AppMain,
    ListProduct,
    AppFooter
  }
}

</script>

<template>
  <AppHeader />
  <AppMain />
  <ListProduct />
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
