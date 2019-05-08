<template>
  <nav class="navbar container is-paddingless" role="navigation" aria-label="main navigation">
    <div class="navbar-brand">
      <nuxt-link to="/" class="navbar-item"><strong>Invest Review</strong></nuxt-link>

      <a
        role="button"
        class="navbar-burger burger"
        aria-label="menu"
        aria-expanded="false"
        data-target="navbarBasicExample"
      >
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
      </a>
    </div>

    <div id="navbarBasicExample" class="navbar-menu">
      <div class="navbar-start">

        <nuxt-link to="/code" class="navbar-item">Kode Referal</nuxt-link>

        <div class="navbar-item has-dropdown is-hoverable">
          <a class="navbar-link">More</a>

          <div class="navbar-dropdown">
            <nuxt-link to="about" class="navbar-item">About</nuxt-link>
            <hr class="navbar-divider">
            <a class="navbar-item" target="_blank" href="https://github.com/puterakahfi/refview-invest/issues">Report an issue</a>
          </div>
        </div>
      </div>

    </div>
  </nav>
</template>


<style scoped>
.navbar {
  left: 0;
  right: 0;
  background-color: transparent;
  padding-top: 20px;
  padding-bottom: 20px;
  height: auto;
}
</style>