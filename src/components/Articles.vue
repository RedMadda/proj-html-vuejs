<template>
  <section class="playlists">
    <div class="container">
      <div class="row playLisHead">
        <div class="col-10">
          <span>Latest articles</span>
        </div>
        <div class="col-2 videos">
          <p id="viewLink">
            <a href="#"
              >Read all articles <i class="chevIco bi bi-chevron-right"></i
            ></a>
          </p>
        </div>
      </div>
      <div class="row justify-content-evenly">
        <ArticlCard v-for="(el, i) in content" :key="i" :det="el" />
      </div>
    </div>
  </section>
</template>

<script>
import ArticlCard from "../components/ArticlCard.vue";
import content from "@/data/ArtContent.js";
export default {
  name: "Articles",
  components: {
    ArticlCard,
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
