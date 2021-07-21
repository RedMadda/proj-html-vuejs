<template>
  <div class="main-wrapper">
   
    <!-- section with three cards -->
      <ProvidedService />
      <!-- section with quote and its author's infos -->
      <Inspirational />
      <!-- online advice -->
      <OnlineAdv />

    </div>
 
</template>

<script>
import ProvidedService from "../components/ProvidedService.vue";
import Inspirational from "../components/Inspirational.vue"
import OnlineAdv from "../components/OnlineAdv.vue"

export default {
  name: "Main",
  components: {
    ProvidedService,
    Inspirational,
    OnlineAdv
  },
};
</script>

<style lang="scss" scoped></style>
