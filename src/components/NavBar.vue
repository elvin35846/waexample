<template>
  <div>
    <div class="nav-bar">
      <div class="nav-bar__logo">EA.</div>
      <ul class="nav-bar__link">
        <li v-for="(item, index) in navData" :key="index" class="nav-bar__link__li">
          <a :href="item.url">{{item.title}}</a>
        </li>
      </ul>
    </div>
    <div class="nav-mobile">
      <div class="nav-mobile__icon">
        <span class="material-icons nav-mobile__icon__menu" @click="openNavMobile=!openNavMobile">{{openNavMobile ? 'close' : 'menu'}}</span>
      </div>
      <ul class="nav-mobile__ul" :style="{'top': openNavMobile ? '0' : '-410px'}" >
        <li v-for="(item, i) in navData" :key="i" class="nav-mobile__ul__li" @click="openNavMobile=!openNavMobile">
          <a :href="item.url">{{item.title}}</a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "HeaderComponent",
  data() {
    return {
      openNavMobile: false,
      navData: [
        { title: "Home", url: "/" },
        { title: "About Us", url: "#about" },
        { title: "Services", url: "#services" },
        { title: "Resume", url: "#resume" },
        { title: "Portfolio", url: "#portfolio" },
        { title: "Pricing", url: "#pricing" },
        { title: "Contact Us", url: "#contact" },
      ],
    };
  },
};
</script>
