<template>
  <v-app id="gnb" left-fixed-sidebar>
    <Navbar/>
    <nuxt/>
  </v-app>
</template>

<script>
import Navbar from '~components/Nav/Navbar.vue'

export default {
  components: {
    Navbar
  }
}
</script>
<style>

</style>
