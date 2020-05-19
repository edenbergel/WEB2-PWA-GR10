<template>
  <div id="app">
    <div id="nav">
      <img alt="Vue logo" src="../src/assets/logo.svg">   

      <div class="nav_link">
        <router-link to="/">Home</router-link>
        <router-link to="/listing">Articles</router-link>
      </div>
    </div>
    <router-view/>
  </div>
</template>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,400;0,700;0,900;1,900&display=swap');

body {
  font-family: 'Roboto', sans-serif;
}

#app {
  text-align: center;
}

#nav {
  display: flex;
  justify-content: space-between;
}

#nav a {
  font-weight: bold;
  color: #000;
  text-decoration: none;

  +a {
    margin-left: 1rem;
  }
}

#nav a.router-link-exact-active {
  color: #DC904D;
}
</style>