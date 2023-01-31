<template>
  <div class="wrapper" v-if="fillNews">
    <div class="title-news">
      {{ fillNews.title }}
    </div>
    <div class="time-news">Date: {{ fillNews.dateAdded }}</div>
    <div class="img-news">
      <img :src="`${fillNews.path}`" />
    </div>
    <div class="content-news">
      {{ fillNews.content }}
    </div>
  </div>
</template>
<script>
import NewsService from "../services/news.service";
export default {
  components: { NewsService },

  data() {
    return { news: {} };
  },
  computed: {
    fillNews() {
      return this.news;
    },
  },
  methods: {
    async retrieveNews() {
      try {
        this.news = await NewsService.get(this.$route.params.id);
        this.news.dateAdded = this.news.dateAdded.split("T")[0];
      } catch (error) {
        console.log(error);
      }
    },
  },
  mounted() {
    this.retrieveNews();
  },
};
</script>
<style scoped>
.wrapper {
  margin-top: 100px;
  width: 100%;
  min-height: 50vh;
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 32px;
  flex-direction: column;
}
.title-news {
  font-weight: bolder;
  font-size: 22px;
}
.img-news img {
  width: 100%;
  object-fit: contain;
  border-radius: 8px;
}
.content-news {
  max-width: 800px;
  color: #747474;
  margin-bottom: 100px;
}
</style>