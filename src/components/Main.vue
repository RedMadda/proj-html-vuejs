<template>
  <div class="main-wrapper">
    <!-- section with three cards -->
    <ProvidedService />
    <!-- section with quote and its author's infos -->
    <Inspirational />
    <!-- online advice -->
    <OnlineAdv />
    <!-- featured videos -->
    <Playlists />
    <!-- subscribe with email -->
    <SubsEmail />
    <!-- other section about available services -->
    <AgainServices />
  </div>
</template>

<script>
import ProvidedService from "../components/ProvidedService.vue";
import Inspirational from "../components/Inspirational.vue";
import OnlineAdv from "../components/OnlineAdv.vue";
import Playlists from "../components/Playlists.vue";
import SubsEmail from "../components/SubsEmail.vue";
import AgainServices from "../components/AgainServices.vue";

export default {
  name: "Main",
  components: {
    ProvidedService,
    Inspirational,
    OnlineAdv,
    Playlists,
    SubsEmail,
    AgainServices,
  },
};
</script>

<style lang="scss" scoped></style>
