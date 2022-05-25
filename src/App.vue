<template>
  <Nav></Nav>
  <slider></slider>
  <the-band></the-band>
  <tour-date></tour-date>
  <Contact></Contact>
  <img src="./assets/imgs/map.jpg" alt="map">
  <Footer></Footer>
</template>

<script>
import Nav from './components/Nav.vue'
import slider from './components/silder.vue'
import TheBand from './components/TheBand.vue'
import TourDate from './components/TourDate.vue'
import Contact from './components/Contact.vue'
import Footer from './components/Footer.vue'
export default {
  components: {
    Nav,
    slider,
    TheBand,
    TourDate,
    Contact,
    Footer,
}
}
</script>

<style>


</style>
