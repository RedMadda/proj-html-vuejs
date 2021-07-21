<template>
  <div class="onlineTxt ms-5 ps-4 my-5 py-5">
    <!-- colored p -->
    <p class="colP">{{ det.pCol }}</p>
    <h2>{{ det.h2 }}</h2>
    <!-- all that logo and youtube stuff -->
    <div class="logViews align-items-center py-4">
      <!-- this is the logo -->
      <img :src="require('@/assets/img/' + det.thLogo)" alt="Theme logo" />
      <!-- wrapper for aligning after, i hope -->
      <div class="viewsTxt">
        <p class="small pb-1">{{ det.smalTxt }}</p>
        <!-- border red/grey -->
        <i class="bi bi-youtube youtube px-1"></i>
        <span class="yTub pe-1">{{ det.spanYT }}</span>
        <span class="views px-1">{{ det.vis }}</span>
      </div>
    </div>
    <!-- last par -->
    <p class="motiv">{{ det.p }}</p>
    <!-- btn -->
    <button class="tubeBtn rounded-pill font-weight-bold my-3">
      <i class="bi bi-youtube"></i>
      {{ det.btnTubText }}
    </button>
  </div>
</template>

<script>
export default {
  name: "OnlineAdvTxt",
  props: {
    det: Object,
  },
};
</script>

<style lang="scss" scoped>
@import "../style/mixins.scss";

.colP {
  color: #4154ff;
  font-size: 1.5rem;
  font-weight: 500;
}

h2 {
  font-size: 3rem;
  width: 70%;
}

.logViews {
  display: flex;

  .viewsTxt {
    line-height: 0rem;
    font-size: 0.9rem;

    .small {
      font-weight: 500;
      color: #98939f;
    }

    .youtube,
    .yTub {
      background-color: #d4353d;
      padding: 4px;
      color: white;
      border: 1px solid #d4353d;
    }

    .youtube {
      border-top-left-radius: 3px;
      border-bottom-left-radius: 3px;
    }

    .views {
      font-size: 0.7rem;
      font-weight: 500;
      color: #98939f;
      padding: 5px 4px;
      border-top: 1px solid #98939f;
      border-bottom: 1px solid #98939f;
      border-right: 1px solid #98939f;
      border-top-right-radius: 3px;
      border-bottom-right-radius: 3px;
    }
  }
}

.motiv {
  font-size: 1.5rem;
  color: #716c77;
}

.tubeBtn {
  @include btn(15px 45px, none, #ff414b, white);

  &:hover {
    @include btn(15px 45px, 2px dotted #cc2e36, #ff414b, white);
  }
}
</style>
