<template>
  <div id="app">
    <div class="navbar-container">
      <div class="navbar-content">
        <router-link to="/">
          <i class="bx bxs-home bx-sm"></i>
        </router-link>
        <router-link to="/cesta">
          <i class="bx bxs-cart bx-sm"></i>
        </router-link>
        <router-link to="/favoritos">
          <i class="bx bxs-star bx-sm"></i>
        </router-link>
        <router-link to="/historial">
          <i class="bx bx-history bx-sm"></i>
        </router-link>
      </div>
    </div>
    <router-view />
  </div>
</template>

<style lang="less">
  * {
    font-family: 'Josefin Sans', sans-serif;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
.navbar-container {
  width: 100%;
  position: fixed;
  bottom: 0;
  .navbar-content {
    display: flex;
    justify-content: space-between;
    padding: 20px;
    a {
      color: rgb(163, 163, 163);
      &.router-link-exact-active {
        color: rgb(255, 131, 62);
      }
    }
  }
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
