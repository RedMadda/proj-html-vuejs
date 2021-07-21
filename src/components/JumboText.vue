<template>
  <section class="jumbo, container">
    <div class="row">
      <!-- text -->
      <span class="mt-5 pt-5">{{ details.text1 }}</span>
      <h1>{{ details.h1 }}</h1>
      <!-- imgs -->
      <div class="img-wrapper">
        <img src="@/assets/img/yelloWave.png" alt="single wave icon" />
        <i class="iPlay bi bi-caret-right-fill"></i>
      </div>
      <!-- text -->
      <p>{{ details.text2 }}</p>
      <!-- buttons -->
      <div class="wrapper-btn">
        <button class="tubeBtn rounded-pill font-weight-bold my-3">
          <i class="bi bi-youtube"></i>&nbsp;
          {{ details.btnTubeText }}
        </button>
        <button class="buyBtn rounded-pill ms-3">
          {{ details.btnBuyText }}
          <i class="bi bi-arrow-right-short"></i>
        </button>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "JumboText",
  props: ["details"],
};
</script>

<style lang="scss" scoped>
@import "../style/mixins.scss";

.container {
  flex-direction: column;
  align-content: flex-start;
  color: white;

  span {
    color: #cd353d;
    font-weight: 500;
    font-size: 1.9rem;
  }

  h1 {
    font-size: 4rem;
  }

  img {
    height: 50px;
    width: 200px;
  }

  .iPlay {
   @include playBtn();
   position: absolute;
   right: 22%;
   top:45%;
  }

  .tubeBtn {
    @include btn(15px 35px, none);

    &:hover {
      @include btn(15px 35px, none, #ff414b, white);
    }
  }

  .buyBtn {
    @include btn(15px 35px, 2px solid rgb(75, 73, 78), black);

    i.bi {
      font-size: 1.5rem;
      position: absolute;
      line-height: 0;
    }

    &:hover {
      @include btn(15px 35px, none, white, black);
    }
  }
}
</style>
