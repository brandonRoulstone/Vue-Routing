<template>
  <nav>
    <router-link to="/">Home</router-link>
    <router-link to="/about">About</router-link>
    <router-link to="/product">Professions</router-link>
    <!-- <router-link to="/personal">Personal</router-link> -->
  </nav>
  <!-- Outlet for all existing nodes  -->
  <router-view/>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
  position: fixed;
  width: 100%;
  display: flex;
  flex-direction: column;
  top: 50%;
  right: 42%;
}

nav a {
  font-weight: bold;
  margin-bottom: 30px;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
