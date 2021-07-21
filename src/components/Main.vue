<template>
  <div class="main-wrapper">
   
    <!-- section with three cards -->
      <ProvidedService />
      <!-- section with quote and its author's infos -->
      <Inspirational />
      <!-- online advice -->
      
    </div>
 
</template>

<script>
import ProvidedService from "../components/ProvidedService.vue";
import Inspirational from "../components/Inspirational.vue"
export default {
  name: "Main",
  components: {
    ProvidedService,
    Inspirational
  },
};
</script>

<style lang="scss" scoped></style>
