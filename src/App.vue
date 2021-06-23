<template>
  <div id="app">
    <div id="nav">
      <router-view />
    </div>
    <div class="select-btn">
      <router-link to="/">甜爱圈</router-link> |
      <router-link to="/about">我的</router-link>
    </div>
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.select-btn {
  height: 40px;
  display: flex;
    justify-content: space-evenly;
    align-items: center;
}

#nav {
  padding: 30px;
  height: calc(100vh - 120px);
    overflow: scroll;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
