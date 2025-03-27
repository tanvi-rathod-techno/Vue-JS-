<template>
  <div>
    <button @click="startTour">Home Start Tour</button>
    <div id="v-step-0">Welcome to Home Page</div>
    <ProductTour ref="tourComponent" />
  </div>
</template>

<script>
import { ref, nextTick } from 'vue';
import ProductTour from '@/components/ProductTour.vue';

export default {
    name:'HomePage',
    components: {
    ProductTour,
  },
  setup() {
    const tourComponent = ref(null);
    const startTour = () => {
      nextTick(() => {
        if (tourComponent.value) {
          tourComponent.value.startTour();
        } else {
          console.error('ProductTour component is not ready.');
        }
      });
    };
    return { tourComponent, startTour };
  },
};
</script>
