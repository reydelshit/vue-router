<template>
  <div id="nav">
    <router-link to="/">Home</router-link> 
    <router-link :to="{ name: 'About'}">About</router-link> 
    <router-link :to="{ name: 'Jobs'}">Jobs</router-link>
  </div>
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

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
  text-decoration: none;
  font-size: 1.5rem;
  padding: 0.3em;
  border-radius: 4px;
}

#nav a.router-link-exact-active {
  color: #42b983;
  border: 2px solid #42b983;
}
</style>
