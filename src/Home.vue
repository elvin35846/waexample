<template>
  <div class="home-block">
    <NavBar />
    <HeaderComponent />
    <AboutComponent />
    
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent'
import AboutComponent from './components/AboutComponent'
import NavBar from './components/NavBar'
export default {
  components: {
    HeaderComponent,
    AboutComponent,
    NavBar
  },
}
</script>

<style lang="scss">
  @import './assets/style/main.scss';
</style>