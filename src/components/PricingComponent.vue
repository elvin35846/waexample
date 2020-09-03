<template>
  <div class="pricing-block" id="pricing">
    <h1 class="pricing-block__title">Pricing</h1>
    <p class="pricing-block__p1">Prices Of Our Works</p>
    <div class="pricing-block__line-decor">
      <hr class="pricing-block__line-decor__normal" />
      <hr class="pricing-block__line-decor__bold" />
    </div>
    <div class="pricing-block__content">
      <div v-for="(colors, i) in priceColor" :key="i">
        <Price :price=priceData :colors=colors />
      </div>
    </div>
  </div>
</template>

<script>
import Price from './Price'
export default {
  components: {
    Price,
  },
  data() {
    return {
      priceData: [
        "Web Design",
        "Interface Design",
        "Web Development",
        "UI Design",
        "Motion Graphic",
        "SEO Optimize",
      ],
      priceColor: [
        '#ff6331',
        '#803dfb',
        '#f5276c'
      ]
    }
  },
}
</script>