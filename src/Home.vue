<template>
  <div class="home-block">
    <NavBar />
    <HeaderComponent />
    <AboutComponent />
    <ServicesComponent />
    <!-- <ResumeComponent /> -->
    <PortfolioComponent />
    <PricingComponent />
    <ContactComponent />
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent'
import AboutComponent from './components/AboutComponent'
import ServicesComponent from './components/ServicesComponent'
// import ResumeComponent from './components/ResumeComponent'
import PortfolioComponent from './components/PortfolioComponent'
import PricingComponent from './components/PricingComponent'
import ContactComponent from './components/ContactComponent'
import NavBar from './components/NavBar'
export default {
  components: {
    HeaderComponent,
    AboutComponent,
    ServicesComponent,
    // ResumeComponent,
    PortfolioComponent,
    PricingComponent,
    ContactComponent,
    NavBar
  },
}
</script>

<style lang="scss">
  @import './assets/style/main.scss';
</style>