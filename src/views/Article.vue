<template>
  <div>
    <div v-if="post" class="article">
      <div class="article--img">
        <img :src="`https://teddyboirin.com/vuejs/${this.$route.params.slug}/${this.$route.params.slug}.jpg`" alt="image" />
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
    };
  },
  beforeCreate() {
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