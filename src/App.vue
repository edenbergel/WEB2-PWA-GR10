<template>
  <div id="app">
    <Header/>
    <router-view/>
  </div>
</template>

<script>
import Header from '@/components/Header.vue'

export default {
  name: 'App',
	components: {
		Header,
	}
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,400;0,700;0,900;1,900&display=swap');

body {
  font-family: 'Roboto', sans-serif;
}

#app {
  text-align: center;
  padding: 2rem;
}
</style>