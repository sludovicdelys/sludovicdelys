<template>
  <div id="app">
    <Portfolio />
  </div>
</template>

<script>
import Portfolio from './views/Portfolio.vue'

export default {
  name: 'App',
  components: {
    Portfolio
  }
}
</script>

<style lang="scss">
@import './styles/main.scss';
</style>
