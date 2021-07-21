<template>
  <div class="container">
    <div class="row">
      <!-- text -->
      <span class="mt-5 pt-5">{{ det.text1 }}</span>
      <h1>{{ det.h2 }}</h1>
      <!-- imgs -->
      <div class="img-wrapper">
        <img src="@/assets/img/yelloWave.png" alt="single wave icon" />
      </div>
    </div>
    <div class="row mb-4">
      <!-- email input -->
      <div class="col-8 form justify-space-around">
        <input
          class="emailInput form-control rounded-pill"
          type="text"
          placeholder="Insert you email...*"
        />
        <!-- button -->
        <button class="subBtn rounded-pill font-weight-bold mx-3">
          Subscribe
        </button>
      </div>
    </div>
    <div class="row">
      <div class="col-8">
        <p class="pEmail">{{ det.text2 }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SubsEmaiTxt.vue",
  props: {
    det: Object,
  },
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
    font-size: 3.3rem;
    width: 65%;
  }

  img {
    height: 50px;
    width: 200px;
  }

  .form {
    display: flex;
    align-items: baseline;

    .emailInput {
      height: 43px;
      padding: 10px 30px;
    }

    .subBtn {
      @include btn(10px 100px, none);
    }
  }

  // last p
  .pEmail {
    font-size: 1.3rem;
    color: #c5c5c5;
  }
}
</style>
