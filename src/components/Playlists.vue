<template>
  <section class="playlists">
    <div class="container">
      <div class="row playLisHead">
        <div class="col-10">
          <span>Featured playlists</span>
        </div>
        <div class="col-2 videos">
          <p id="viewLink">
            <a href="#"
              >View all videos <i class="chevIco bi bi-chevron-right"></i
            ></a>
          </p>
        </div>
      </div>
      <div class="row justify-content-evenly">
        <PlayCard v-for="(el, i) in content" :key="i" :det="el" />
      </div>
    </div>
  </section>
</template>

<script>
import PlayCard from "../components/PlayCard.vue";
import content from "@/data/PlayListsCont.js";
export default {
  name: "Playlists",
  components: {
    PlayCard,
  },
  data() {
    return {
      content,
    };
  },
};
</script>

<style lang="scss" scoped>
.playlists {
  margin: auto;
  margin-top: 150px;

  span {
    font-size: 1.5rem;
    font-weight: 500;
  }
  .videos {
    display: flex;
    align-items: center;

    .chevIco {
      font-size: 0.5rem;
    }
  }
}
</style>
