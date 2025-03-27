<template>
  <div>
    <div data-v-step="2">Profile Section</div>
    <ProductTour ref="tour" />
  </div>
</template>

<script>
import ProductTour from '@/components/ProductTour.vue';

export default {
   name: 'ProfileView',
  components: {
    ProductTour,
  },
  methods: {
    startTour() {
      this.$refs.tour.startTour();
    },
  },
};
</script>
