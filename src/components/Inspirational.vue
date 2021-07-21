<template>
  <section class="quote">
    <QuoteContent v-for="(el, i) in content" :key="i" :details="el" />
  </section>
</template>

<script>
import content from "../data/QuoteInsp.js";
import QuoteContent from "../components/QuoteContent.vue";

export default {
  name: "Inspirational",
  components: {
    QuoteContent,
  },
  data() {
    return {
      content,
    };
  },
};
</script>

<style lang="scss" scoped>
.quote {
  width: 100%;
  height: 113vh;
  background: linear-gradient(to bottom right, #0319ea 5%, #a4063f 95%);
}
</style>
