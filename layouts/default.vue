<template>
  <v-app>
    <Navbar/>
    <v-content>
      <nuxt/>
      <Foot/>
    </v-content>
  </v-app>
</template>
<script>
import Navbar from '~components/Nav/Navbar.vue'
import Foot from '~components/Foot.vue'

export default {
  components: {
    Navbar,
    Foot
  }
}
</script>
<style>

</style>
