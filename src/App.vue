<script>
import AppHeader from './components/AppHeader.vue'
import AppFooter from './components/AppFooter.vue'
import AppBonusComponent from './components/AppBonusComponent.vue'
import AppMain from './components/AppMain.vue'

export default {
  components: {
    AppHeader,
    AppMain,
    AppBonusComponent,
    AppFooter
  },
  data() {
    return {

    }
  }
}
</script>

<template>
  <AppHeader />
  <AppMain />
  <footer>
    <AppBonusComponent />
    <AppFooter />
  </footer>
</template>

<style lang="scss">
@use './style/general.scss';
</style>
