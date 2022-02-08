<template>
  <div id="app">
      <header-box />
  </div>
</template>

<script>
import HeaderBox from './components/HeaderBox.vue'

export default {
  name: 'App',
  components: {
    HeaderBox,
  }
}
</script>

<style lang="scss">
@import './style/main.scss';
@import './style/variables.scss';
</style>
