<template>
  <div class="row">
    <div class="col-md-4" v-for="article in articles" :key="article.id">
      <b-card
        img-src="https://picsum.photos/600/300/?image=25"
        img-alt="Image"
        img-top
        tag="article"
        style="max-width: 20rem"
        class="mb-2"
      >
        <b-card-text>
          <h4>{{ article.title }}</h4>
        {{ article.body }}
        </b-card-text>
      </b-card>
    </div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "Hero",
  data() {
    return {
      articles: [],
    };
  },

  async mounted() {
    const res = await axios.get(`https://jsonplaceholder.typicode.com/posts`);
    this.articles = res.data;
  },
};
</script>

<style>
</style>