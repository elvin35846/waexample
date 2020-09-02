<template>
  <div class="nav-bar">
      <div class="nav-bar__logo">
        EA.
      </div>
      <ul class="nav-bar__link">
        <li v-for="(item, index) in navData" :key="index" class="nav-bar__link__li">
          <a :href="item.url">{{item.title}}</a>
        </li>
      </ul>
    </div>
</template>

<script>
export default {
  name: 'HeaderComponent',
  data() {
    return {
      navData: [
        { title: 'Home', url: '/' },
        { title: 'About Us', url: '#about' },
        { title: 'Services', url: '/' },
        { title: 'Resume', url: '/' },
        { title: 'Portfolio', url: '/' },
        { title: 'Pricing', url: '/' }
      ]
    }
  },
}
</script>
