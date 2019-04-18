<template>
<div id="app">
  <div class="pure-menu">
    <span class="pure-menu-heading">Creative Project 5</span>
    <ul class="pure-menu-list">
      <li class="pure-menu-item">
        <router-link to="/" class="pure-menu-link">Home</router-link>
      </li>
      <li class="pure-menu-item">
        <router-link to="/mypage" class="pure-menu-link">My Page</router-link>
      </li>
    </ul>
  </div>
  <div class="content">
    <router-view />
  </div>
</div>
</template>

<style lang="scss">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 30px;
  a {
    font-weight: bold;
    color: #2c3e50;
    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
.pure-menu-heading {
  color: #fff;
  font-size: 1.2em;
  padding: 20px 20px;
  background-color: #006DD3;
  margin-bottom: 10px;
}

</style>
