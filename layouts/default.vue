<template>
  <v-app id="gnb" left-fixed-sidebar>
    <Navbar/>
    <nuxt/>
    <Foot/>
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
