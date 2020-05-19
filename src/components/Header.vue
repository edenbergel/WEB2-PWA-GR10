<template>
    <div id="nav">
      <img alt="Vue logo" src="../assets/logo.svg">   

      <div class="nav_link">
        <router-link to="/">Home</router-link>
        <router-link to="/listing">Articles</router-link>
      </div>
    </div>
</template>

<script>
export default {
  name: 'Header',
}
</script>

<style lang="scss">
  @import '../scss/header.scss';
</style>