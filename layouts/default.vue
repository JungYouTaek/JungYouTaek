<template>
  <v-app with top-fixed-tollbar left-fixed-sidebar bottom-footer>
    <Navbar/>
    <main>
      <Sidebar/>
      <v-content fluid>
      <nuxt/>
      </v-content>
    </main>
    <Foot/>
  </v-app>
</template>

<script>
import Navbar from '~components/Nav/Navbar.vue'
import Sidebar from '~components/Nav/Sidebar.vue'
import Foot from '~components/Foot.vue'

export default {
  components: {
    Navbar,
    Sidebar,
    Foot
  }
}
</script>
<style>
html, body {
  height: 100%;
}
.content {
  height: 100%;
}
#app {
  height: 100%;
}
.with {
  min-height: 100vh;
  overflow-x: hidden;
}
.with.top-fixed-toolbar {
  padding-top: 64px;
}
</style>
