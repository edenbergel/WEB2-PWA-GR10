<template>
  <div class="about">
   
  
  </div>
</template>

<script>
export default {
  data () {
    return {
      posts: null
    }
  },
  created () {
    fetch('https://jsonplaceholder.typicode.com/posts').then((response) => {
      response.json().then((data) => {
        this.posts = data
      })
    })
  }
}
</script>