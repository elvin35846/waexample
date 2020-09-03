<template>
  <div class="portfolio-block" id="portfolio">
    <h1 class="portfolio-block__title">Portfolio</h1>
    <p class="portfolio-block__p1">Portfolio of My Latest Works</p>
    <div class="portfolio-block__line-decor">
      <hr class="portfolio-block__line-decor__normal" />
      <hr class="portfolio-block__line-decor__bold" />
    </div>
    <ul class="portfolio-block__ul">
      <li class="portfolio-block__ul__li" :class="{active : isActive == item}" v-for="(item, i) in portfolioData" :key="i" @click="isActive = item">{{item}}</li>
    </ul>
    <div class="portfolio-block__content">
      <img src="../assets/img/slid1.jpg" alt="">
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      portfolioData: [
        "Web Design",
        "Interface Design",
        "Web Development",
        "UI Design",
        "Motion Graphic",
        "SEO Optimize",
      ],
      isActive: 'Web Design'
    };
  },
};
</script>