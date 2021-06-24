<template>
  <div class="layout">
    <header class="header">
      <b-navbar>
        <template #brand>
          <b-navbar-item tag="router-link" :to="{ path: '/' }">
            <g-image src="~/img/Rick_and_Morty.png" width="100" fit="contain" />
          </b-navbar-item>
        </template>
        <template #end>
          <b-navbar-item tag="router-link" active :to="{ path: '/personnage' }">
            List des Personnages
          </b-navbar-item>
        </template>
      </b-navbar>
    </header>
    <slot />
    <footer class="footer">
      <div class="content has-text-centered">
        <p>
          Website for test technique of
          <a href="https://www.comptalib.com/">Comptalib</a> use
          <a href="https://rickandmortyapi.com/">Rick & morty API</a>
          Author Théo
        </p>
      </div>
    </footer>
  </div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<style>
body {
  font-family: -apple-system, system-ui, BlinkMacSystemFont, "Segoe UI", Roboto,
    "Helvetica Neue", Arial, sans-serif;
  margin: 0;
  padding: 0;
  line-height: 1.5;
}
.layout {
  max-width: 920px;
  margin: 0 auto;
}
</style>
