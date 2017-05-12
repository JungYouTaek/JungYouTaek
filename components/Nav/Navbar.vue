<template>
  <nav>
    <v-toolbar class="light-green">
      <v-toolbar-side-icon @click.native.stop="sidebar = !sidebar" />
      <v-toolbar-title class="hidden-sm-and-down">영양만점</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn icon dark>
        <v-icon>account_circle</v-icon>
      </v-btn>
      <v-btn icon dark>
        <v-icon>favorite</v-icon>
      </v-btn>
      <v-btn icon dark>
        <v-icon>more_vert</v-icon>
      </v-btn>
    </v-toolbar>
    <v-sidebar left fixed drawer v-model="sidebar">
      <v-list>
        <v-list-item v-for="i in 3" :key="i">
          <v-list-tile>
            <v-list-tile-title>Item {{ i }}</v-list-tile-title>
          </v-list-tile>
        </v-list-item>
      </v-list>
    </v-sidebar>
  </nav>
</template>

<script>
export default {
  data () {
    return {
      sidebar: false
    }
  }
}
</script>

<style lang="css">
</style>
