<script>
import AppHeader from './components/AppHeader.vue'
import AppMain from './components/AppMain.vue'

export default {
  components: {
    AppHeader,
    AppMain,
  }
}

</script>

<template>
  <AppHeader />
  <AppMain />
</template>

<style lang="scss">
@use './styles/partials/variables' as*;
@use './styles/partials/general.scss' as*;

li a {
  color: $primary;
}
</style>
