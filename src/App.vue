<template>
  <div id="app">
    <nav class="navbar navbar-expand-lg navbar-light">
      <div class="container">
        <router-link class="navbar-brand" to="/">Quotes of the day - Levels Conf 2018</router-link>
      </div>
    </nav>
    <transition name="fade">
      <router-view/>
    </transition>
    <div class="container">
      <div class="row">
        <div class="col-12 footer">
          <a class="nav__link" href="https://github.com/B3nnyL">Github</a>
          <a class="nav__link" href="https://twitter.com/_wlfp">@wlfp</a>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
  @import '../node_modules/bootstrap/dist/css/bootstrap.min.css';
  @import './assets/main.css';
  
  #app {
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
  }

  .navbar {
    border-bottom: 2px solid black;
  }

  .navbar-brand {
    font-size: 14px;
    padding: 15px;
  }

  .footer {
    padding: 15px;
    a {
      text-decoration: underline;
    }
  }

  .fade-enter-active,
  .fade-leave-active {
    transition: opacity .5s;
  }

  .fade-enter,
  .fade-leave-to {
    opacity: 0;
  }
</style>
