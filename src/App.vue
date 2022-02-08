<template>
  <div id="app">
      <pre-header :phone="phone_number" />
      <header-box :items="navItems" />
      <jumbotron-box />
      <section-1-content />
      <banner-box :phone="phone_number" />
  </div>
</template>

<script>
import PreHeader from './components/PreHeader.vue'
import HeaderBox from './components/HeaderBox.vue'
import JumbotronBox from './components/JumbotronBox.vue'
import Section1Content from './components/Section1Content.vue'
import BannerBox from './components/BannerBox.vue'

export default {
  name: 'App',
  components: {
    HeaderBox,
    PreHeader,
    JumbotronBox,
    Section1Content,
    BannerBox,
  },
  data() {
      return{
          // PHONE NUMBER
          phone_number: '1-800-555-555',

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
