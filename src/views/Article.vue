<template>
  <div>
    <div class="article">
      <div class="article--img">
        <img :src="`https://picsum.photos/1024/480/?image=${idUrl} `" alt="image" />
      </div>
      <div class="article--content">
        <h1>{{post.title}}</h1>

        {{post.body}}
        <div class="buttons">
            <router-link class="retour"  :to="`/listing/`">Retour</router-link>
        </div>
      </div>
    </div>
  </div>
</template>
<style lang="scss" scoped>
@import url("../scss/article.scss");
</style>
<script>
export default {
  data() {
    return {
      post: null,
      idUrl: parseInt(this.$route.params.slug) + 15 - 1 
    };
  },
  created() {
    fetch(
      `https://jsonplaceholder.typicode.com/posts/${this.$route.params.slug}`
    ).then(response => {
      response.json().then(data => {
        this.post = data;
      });
    });
  }
};
</script>