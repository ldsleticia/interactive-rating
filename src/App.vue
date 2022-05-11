<template>
  <div>
   <RatingComponent/>
   <ThankyouComponent/>
  </div>
</template>

<script>
import RatingComponent from './components/RatingComponent.vue';
import ThankyouComponent from './components/ThankYouComponent.vue';

export default {
  components: {
    RatingComponent,
    ThankyouComponent,
  },
};
</script>
