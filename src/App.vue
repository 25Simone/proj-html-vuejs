<template>
  <div id="app">
      <pre-header />
      <header-box :items="navItems" />
      <jumbotron-box />
  </div>
</template>

<script>
import HeaderBox from './components/HeaderBox.vue'
import JumbotronBox from './components/JumbotronBox.vue'
import PreHeader from './components/PreHeader.vue'

export default {
  name: 'App',
  components: {
    HeaderBox,
    PreHeader,
    JumbotronBox,
  },
  data() {
      return{
          // NAVBAR DATA
          navItems: [
              {
                  id: 'n1',
                  label: 'Home',
                  link: '#',
                  new_tag: false,
              },
              {
                  id: 'n2',
                  label: 'About',
                  link: '#',
                  new_tag: false,
              },
              {
                  id: 'n3',
                  label: 'Prices',
                  link: '#',
                  new_tag: false,
              },
              {
                  id: 'n4',
                  label: 'Courses',
                  link: '#',
                  new_tag: true,
              },
              {
                  id: 'n5',
                  label: 'Locations',
                  link: '#',
                  new_tag: false,
              },
              {
                  id: 'n6',
                  label: 'Blog',
                  link: '#',
                  new_tag: false,
              },
          ],
      }
  }
}
</script>

<style lang="scss">
@import './style/main.scss';
@import './style/variables.scss';
</style>
