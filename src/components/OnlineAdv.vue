<template>
  <section class="onlineAdv">
    <div class="container-fluid pb-5">
      <div class="row position-relative mb-5">
        <div class="col-5">
          <div class="imgWrap position-relative">
            <div class="img position-absolute">
              <i class="iPlay bi bi-caret-right-fill"></i>
            </div>
          </div>
        </div>
        <div class="col-7">
          <OnlineAdvTxt v-for="(el, i) in content" :key="i" :det="el" />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import content from "@/data/OnlineContent.js";
import OnlineAdvTxt from "../components/OnlineAdvTxt.vue";
export default {
  name: "OnlineAdv",
  components: {
    OnlineAdvTxt,
  },
  data() {
    return {
      content,
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../style/mixins.scss";

.onlineAdv {
  height: 80vh;
  width: 99%;

  .imgWrap {
    height: 95vh;
    background-image: linear-gradient(
        to right,
        rgba(14, 13, 13, 0.26) 100%,
        transparent
      ),
      url("~@/assets/img/service15-2x.jpg");
    background-size: 100%;
    top: -50px;
    border-radius: 5px;
    border-bottom-right-radius: 5%;
    background-size: cover;
    background-repeat: no-repeat;

    .img {
      top: 50%;
      left: 47%;
    }
  }

  .iPlay {
    @include playBtn();
    // position: absolute;
    right: 0%;
    top: 0%;
  }
}

.toDelet {
  height: 200px;
}
</style>
