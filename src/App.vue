<template>
  <div id="app">
      <!-- HEADER -->
      <pre-header :phone="phone_number" />
      <header-box :items="navItems" />
      <jumbotron-box />
      <!-- MAIN -->
      <presentation-section id="presentation-section"/>
      <banner-box :phone="phone_number" />
      <courses-section :cards="courses" />
      <analytic-section id="analytic-section" :items="statistics" />
      <instructors-box id="istructors-container" :cards="istructorsList" />
      <testimonials-app :testimonials="testimonialsList" />
      <div id="latest-news-bg">
          <latest-news id="latest-news-content"/>
      </div>
      <newsletter-form />
      <!-- FOOTER -->
      <footer-app :contacts="contactDetails" :coursesLinks="coursesLinks" />
  </div>
</template>

<script>
import PreHeader from './components/PreHeader.vue'
import HeaderBox from './components/HeaderBox.vue'
import JumbotronBox from './components/JumbotronBox.vue'
import PresentationSection from './components/PresentationSection.vue'
import BannerBox from './components/BannerBox.vue'
import CoursesSection from './components/CoursesSection.vue'
import AnalyticSection from './components/AnalyticSection.vue'
import InstructorsBox from './components/IstructorsBox.vue'
import TestimonialsApp from './components/TestimonialsApp.vue'
import LatestNews from './components/LatestNews.vue'
import NewsletterForm from './components/NewsleterForm.vue'
import FooterApp from './components/FooterApp.vue'

export default {
  name: 'App',
  components: {
    HeaderBox,
    PreHeader,
    JumbotronBox,
    PresentationSection,
    BannerBox,
    CoursesSection,
    AnalyticSection,
    InstructorsBox,
    TestimonialsApp,
    LatestNews,
    NewsletterForm,
    FooterApp,
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

          // COURSES LIST
          courses: [
              {
                  id: 'c1',
                  name: 'Pass Pluse',
                  image: 'courses-passplus.jpg',
              },
              {
                  id: 'c2',
                  name: 'Intensive Course',
                  image: 'course-intensive.jpg',
              },
              {
                  id: 'c3',
                  name: 'Instructors',
                  image: 'courses-instructor.jpg',
              },
          ],

          // ISTRUCTORS
          istructorsList: [
              {
                  id: 'i1',
                  name: 'Mike Hart',
                  overview: 'Lorem ipsum dolor sit amet,consectetur adipiscing elit.',
                  image: 'mikehart.jpg',
              },
              {
                  id: 'i2',
                  name: 'John Smith',
                  overview: 'Lorem ipsum dolor sit amet,consectetur adipiscing elit.',
                  image: 'johnsmith.jpg',
              },
              {
                  id: 'i3',
                  name: 'Angela Hart',
                  overview: 'Lorem ipsum dolor sit amet,consectetur adipiscing elit.',
                  image: 'angelahart.jpg',
              },
          ],

          // STATISTICS
          statistics: [
              {
                  value: '95%',
                  show_id: '95',
                  rate_name: 'pass rate',
              },
              {
                  value: '100%',
                  show_id: '100',
                  rate_name: 'referral rate',
              },
              {
                  value: '0%',
                  show_id: '0',
                  rate_name: 'accident rate',
              },
          ],

          //TESTIMONIALS
          testimonialsList: [
              {
                  id: 't1',
                  image:'sophia.png',
                  name: 'Sophia Jones',
                  overview: 'Avada Driving School really helped build my confidence behind thw wheel and with driving in general, and they got me a first time pass! Highly recommended.'
              },
              {
                  id: 't2',
                  image:'harold.png',
                  name: 'Harold Clark',
                  overview: 'Avada Driving School really helped build my confidence behind thw wheel and with driving in general, and they got me a first time pass! Highly recommended.'
              },
              {
                  id: 't3',
                  image:'kelly.png',
                  name: 'Kelly Winston',
                  overview: 'Avada Driving School really helped build my confidence behind thw wheel and with driving in general, and they got me a first time pass! Highly recommended.'
              },
              {
                  id: 't4',
                  image:'grant.png',
                  name: 'Grant Bishop',
                  overview: 'Avada Driving School really helped build my confidence behind thw wheel and with driving in general, and they got me a first time pass! Highly recommended.'
              },
              {
                  id: 't5',
                  image:'kate.png',
                  name: 'Kate Wilson',
                  overview: 'Avada Driving School really helped build my confidence behind thw wheel and with driving in general, and they got me a first time pass! Highly recommended.'
              },
          ],

          // CONTACT DETAILS
          contactDetails: [
              {
                  id: 'co1',
                  fa_icon: 'fas fa-home',
                  text: '12345 North Main Street, New York, NY 555555',
              },
              {
                  id: 'co2',
                  fa_icon: 'fas fa-phone',
                  text: '1.800.555.6789',
              },
              {
                  id: 'co3',
                  fa_icon: 'far fa-envelope',
                  text: 'info@your-domain.com',
              },
              {
                  id: 'co4',
                  fa_icon: 'fas fa-link',
                  text: 'Theme-Fusion.com',
              },
          ],

          // COURSES LINKS
          coursesLinks: [
              {
                  id: 'cl1',
                  name: 'Pass Plus',
                  link: '#',
              },
              {
                  id: 'cl2',
                  name: 'Intensive Course',
                  link: '#',
              },
              {
                  id: 'cl3',
                  name: 'Automatic',
                  link: '#',
              },
              {
                  id: 'cl4',
                  name: 'Instructor Training',
                  link: '#',
              },
          ],
      }
  }
}
</script>

<style lang="scss">
@import './style/main.scss';
@import './style/variables.scss';

#presentation-section{
    position: relative;
    top: -40px;
}

#analytic-section{
    position: relative;
    top: -150px;
}
#istructors-container{
    position: relative;
    bottom: -150px;
}
#latest-news-bg{
    background: url('./assets/images/latestnews-background.jpg');
    background-size: cover;
    padding-bottom: 60px;
    #latest-news-content{
        position: relative;
        top: -40px;
    }
}
</style>
