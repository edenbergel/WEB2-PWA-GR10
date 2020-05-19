<template>
  <div>
    <h1>{{ post.title }}</h1>
    <h1>test</h1>
    <p>{{ post.body }}</p>
  </div>
  
</template>

<script>
export default {
  data () {
    return {
      post: null
    }
  },
  created () {
    fetch(`https://jsonplaceholder.typicode.com/posts/${this.$route.params.slug}`).then((response) => {
      response.json().then((data) => {
        this.post = data
      })
    })
  }
}
</script>