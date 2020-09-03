<template>
  <div
    class="services-card"
    :style="{ 'borderColor': color, 'backgroundColor': isHover ? '#ffffff' : color, 'color': !isHover ? '#ffffff' : color }"
    @mouseover="isHover = true"
    @mouseout="isHover = false"
  >
    <span class="material-icons services-card__icon">{{icon}}</span>
    <h3 class="services-card__title">{{title}}</h3>
    <p class="services-card__text">{{text}}</p>
  </div>
</template>

<script>
export default {
  props: {
    color: String,
    icon: String,
    title: String,
    text: String
  },
  data() {
    return {
      isHover: false
    }
  },
}
</script>