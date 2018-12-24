<template>
  <section class="system-header">
    <section class="logo-mode">
      <router-link to="/index.html">
        <img src="@/assets/images/logo.png" alt="珠海税务平台">
      </router-link>
    </section>
  </section>
</template>

<style lang="scss">
  #app {
    position: relative;
    width: 100%;
    height: 100%;
    font-family: $fontFamily;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
  }
  .system-header {
    position: relative;
    width: 100%;
    height: 100%;
  }
  .logo-mode {
    float: left;
    position: relative;
    display: table;
    height: 100%;
    > a {
      display: table-cell;
      vertical-align: middle;
      text-decoration: none;
    }
  }
</style>

