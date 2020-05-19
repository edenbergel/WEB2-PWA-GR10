<template>
  <div class="carousel-vue">
    <div class="title">
      <h2>Nos derniers articles</h2>
      <h2>Nos derniers articles</h2>
    </div>

    <div class="auto">
      <b-carousel
        id="carousel-fade"
        style="text-shadow: 0px 0px 2px #000"
        fade
        indicators
        img-width="1024"
        img-height="480"
      >
        <router-link v-for="(post, index) in posts" :to="`/article/${ post.id }`" :key="post.id">
          <b-carousel-slide
            :caption="post.title"
            :img-src="`https://picsum.photos/1024/480/?image=${index}`"
            
          >
            <router-link class="read"  :to="`/article/${ post.id }`">Lire l'article</router-link>
          </b-carousel-slide>
         
        </router-link>
        
      </b-carousel>
    </div>
  </div>
</template>
<style lang="scss" scoped>
@import url("../scss/articles.scss");
</style>

<script>
export default {
  data() {
    return {
      posts: null
    };
  },
  created() {
    fetch("https://jsonplaceholder.typicode.com/posts/?_limit=5").then(
      response => {
        response.json().then(data => {
          this.posts = data;
        });
      }
    );
  }
};
</script>