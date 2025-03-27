<template>
  <v-tour name="myTour" :steps="steps" />
</template>

<script>
export default {
  data() {
    return {
      steps: [
        {
          target: '#v-step-0',
          header: { title: 'Welcome to the App!' },
          content: `Discover <strong>Vue3 Tour</strong>!`,
        },
        {
          target: '.v-step-1',
          content: 'An awesome plugin made with Vue.js!',
        },
        {
          target: '[data-v-step="2"]',
          content: "Try it, you'll love it!",
          params: { placement: 'top' },
        },
      ],
    };
  },
  methods: {
    startTour() {
      if (this.$tours && this.$tours.myTour) {
        this.$tours.myTour.start();
      } else {
        console.error('Vue3 Tour instance not found.');
      }
    },
  },
};
</script>

<style scoped>
.v-step {
    background: #ffcb00;
    color: #fff;
    max-width: 320px;
    border-radius: 3px;
    box-shadow: #0000 0 0, #0000 0 0, #0000001a 0 4px 6px -1px, #0000000f 0 2px 4px -1px;
    padding: 10px;
    pointer-events: auto;
    text-align: center;
    z-index: 10000;
}
</style>
