<template>
  <section class="servAgain py-5"> 
    <div class="container pt-5">
      <div class="row justify-content-evenly">
        <AgainServCard v-for="(el, i) in content" :key="i" :det="el" />
      </div>
    </div>
  </section>
</template>

<script>
import content from "../data/AgainServCont";
import AgainServCard from "../components/AgainServCard.vue";
export default {
  name: "AgainServices",
  components: {
    AgainServCard,
  },
  data() {
    return {
      content,
    };
  },
};
</script>

<style lang="scss" scoped>
.servAgain {
  height: 89vh;
  width:100%;
  background-color: black;
  color: white;
}
</style>
