<template>
  <div class="price-block">
    <div class="price-block__header" :style="{'background-color': colors}">
      <h2 class="price-block__header__h2">Basic</h2>
      <p class="price-block__header__p1">$70</p>
      <p class="price-block__header__p1">Basic price</p>
    </div>
    <ul class="price-block__ul">
      <li class="price-block__ul__li" v-for="(item, i) in price" :key="i">
        <span class="material-icons price-block__ul__li__doneIcon">done</span>
        {{item}}
      </li>
    </ul>
    <div class="price-block__btn-block">
      <router-link to="#" tag="a" class="price-block__btn-block__btn2" 
      :style="{'background-color': isHover ? '#ffffff' : colors, 'border-color': colors, 'color': !isHover ? '#ffffff' : colors}"
      @mouseover.native="isHover = true"
      @mouseout.native="isHover = false" >BUY </router-link>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    price: Array,
    colors: String
  },
  data() {
    return {
      isHover: false
    }
  },
};
</script>