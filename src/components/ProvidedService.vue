<template>
  <section class="Service">
    <div class="centWrap container position-absolute">
      <div class="row justify-content-evenly">
        <ServiceCard v-for="(el, i) in servCardData"  :key="i" :details="el" />
       </div>
    </div>
  </section>
</template>

<script>
import ServiceCard from "../components/ServiceCard.vue";
import servCardData from "../data/ServiceContent.js";

export default {
  name: "ProvidedService",
  components: {
    ServiceCard,
  },

  data() {
    return {
      servCardData,
    };
  },
};
</script>

<style lang="scss" scoped>

.centWrap{
  left:50%;
  transform: translateX(-50%);
}

</style>
