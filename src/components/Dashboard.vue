<template>
  <div>
    <div class="v-step-1">Dashboard Section</div>
    <ProductTour ref="tour" />
  </div>
</template>

<script>
import ProductTour from '@/components/ProductTour.vue';

export default {
  name: 'UserDashboard',
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
