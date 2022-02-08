<template>
  <div id="app">
      <pre-header />
      <header-box />
  </div>
</template>

<script>
import HeaderBox from './components/HeaderBox.vue'
import PreHeader from './components/PreHeader.vue'

export default {
  name: 'App',
  components: {
    HeaderBox,
    PreHeader,
  }
}
</script>

<style lang="scss">
@import './style/main.scss';
@import './style/variables.scss';
</style>
