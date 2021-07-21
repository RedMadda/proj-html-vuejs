<template>
  <section class="email">
    <div class="container-fluid bck">
      <SubsEmaiTxt v-for="(el, i) in content" :key="i" :det="el" />
    </div>
  </section>
</template>

<script>
import content from "@/data/SubEmailCont.js";
import SubsEmaiTxt from "../components/SubsEmaiTxt.vue";
export default {
  name: "SubsEmail",
  components: {
    SubsEmaiTxt,
  },
  data() {
    return {
      content,
    };
  },
};
</script>

<style lang="scss" scoped>
section {
  margin-top: 70px;
}
.bck {
  height: calc(89vh - 90px);
  background-image: linear-gradient(to right, black 35%, transparent),
    url("~@/assets/img/banner1-2x.jpg");
  background-size: 100%;
  background-repeat: no-repeat;
}
</style>
