<template>
  <div class="wrapper">
    <div
      class="heading-news font-weight-bolder ml-5 mt-5"
      style="font-size: 22px"
    >
      Tin tức xe đạp
    </div>
    <div class="wrapper-news mt-5 mb-5 ml-5 mr-5 d-flex flex-wrap">
      <div v-for="(item, index) in fillNews" :key="index" class="box-news mt-4">
        <router-link
          class="router_link text-decoration-none"
          style="color: black"
          :to="{
            name: 'DetailNewsView',
            params: { id: item._id },
          }"
        >
          <div class="img-news">
            <img :src="`${item.path}`" />
          </div>
          <div class="body-news p-3 mt-2">
            <div class="time-news" style="font-size: 12px; color: #747474">
              {{ ` ${changeDate(item.dateAdded)}` }}
            </div>
            <div class="name-news font-weight-bolder">
              {{ item.title }}
            </div>
          </div>
        </router-link>
      </div>
    </div>
  </div>
</template>
<style scoped>
.wrapper {
  margin-top: 100px;
  width: 100%;
  min-height: 50vh;
}
.wrapper-news {
  min-height: 40vh;
  gap: 12px;
}
.box-news {
  width: 320px;
  border-radius: 4px;
  box-shadow: 0 3px 10px rgb(0 0 0 / 0.2);
}
.img-news {
  width: 100%;
}
.img-news img {
  width: 100%;
  height: 140px;
}
</style>
<script>
import NewsService from "../services/news.service";
export default {
  components: { NewsService },

  data() {
    return { news: [] };
  },
  computed: {
    fillNews() {
      return this.news;
    },
  },
  methods: {
    async retrieveNews() {
      try {
        this.news = await NewsService.getAll();
      } catch (error) {
        console.log(error);
      }
    },
    changeDate(date) {
      return date.split("T")[0];
    },
  },
  mounted() {
    this.retrieveNews();
  },
};
</script>