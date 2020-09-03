<template>
  <div class="services-block" id="services">
    <h1 class="services-block__title">Services</h1>
    <p class="services-block__p1">What Do We Offer?</p>
    <div class="services-block__line-decor">
      <hr class="services-block__line-decor__normal">
      <hr class="services-block__line-decor__bold">
    </div>
    <div class="services-block__content">
      <div v-for="(item, i) in servicesData" :key="i">
        <ServicesCard :title=item.title :text=item.text :color=item.color :icon=item.icon />
      </div>
    </div>
  </div>
</template>

<script>
import ServicesCard from './ServicesCard.vue'
export default {
  components: {
    ServicesCard,
  },
  data() {
    return {
      servicesData: [
        { icon: 'computer', color: '#803afb', title: 'Web Design', text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Numquam porro quia, nisi saepe dolore omnis.' },
        { icon: 'library_books', color: '#ffc50c', title: 'Interface Design', text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Numquam porro quia, nisi saepe dolore omnis.' },
        { icon: 'developer_board', color: '#ec407a', title: 'Web Development', text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Numquam porro quia, nisi saepe dolore omnis.' },
        { icon: 'satellite', color: '#ff6331', title: 'UI Design', text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Numquam porro quia, nisi saepe dolore omnis.' },
        { icon: 'ondemand_video', color: '#03acf8', title: 'Motion Graphic', text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Numquam porro quia, nisi saepe dolore omnis.' },
        { icon: 'insights', color: '#49b846', title: 'SEO Optimize', text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Numquam porro quia, nisi saepe dolore omnis.' }
      ]
    }
  },
}
</script>