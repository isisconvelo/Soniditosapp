<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">isis</router-link> |
      <router-link to="/about">soniditos</router-link>
    </div>
    <router-view/>
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  background-color: #2c3e50;

  height: 100%;
  width: 100%;
  margin: 0;
}

html, body{ 
  height: 100%;
  width: 100%;
  margin: 0;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
