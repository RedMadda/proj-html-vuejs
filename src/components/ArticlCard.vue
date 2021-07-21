<template>
  <div class="playCard position-relative col-3 text-center mt-5 mb-4">
    <img
      class="playImg pb-4"
      :src="require('@/assets/img/' + det.bckNam + '.jpg')"
      alt="Workout tutorial"
    />
    <!-- play -->
    <div><i class="playBtn position-absolute bi bi-caret-right-fill"></i></div>
    <!-- text -->
    <h3>{{ det.h3 }}</h3>
    <p>{{ det.p }}</p>
  </div>
</template>

<script>
export default {
  name: "ArticlCard",
  props: {
    det: Object,
  },
};
</script>

<style lang="scss" scoped>
@import "@/style/mixins.scss";

.playImg {
  width: 300px;
  border-bottom-right-radius: 70px;
}

.playBtn {
  @include playBtn(0.5rem, 1rem);
  top: 40%;
  left: 45%;
}

h3 {
  font-size: 1.5rem;
}

p {
  color: #4154ff;
  font-weight: 500;
}
</style>
