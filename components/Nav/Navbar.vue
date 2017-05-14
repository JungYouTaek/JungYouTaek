<template>
  <nav id="gnb" fixed>
    <v-toolbar class="light-green">
      <v-toolbar-side-icon @click.native.stop="sidebar = !sidebar" />
      <v-toolbar-title class="hidden-xs-only"><a href="/">영양만점</a></v-toolbar-title>
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
    <v-sidebar v-model="sidebar" left fixed>
      <v-list>
        <v-list-item v-for="list in lists" :key="list.id">
          <v-list-tile>
            <v-list-tile-title>{{ list.name }}</v-list-tile-title>
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
      sidebar: true,
      lists: [
        { name: '홈페이지 소개' },
        { name: '테스트 해보기' },
        { name: '개인정보' }
      ]
    }
  }
}
</script>

<style lang="css">
a {
  text-decoration: none;
  color: white
}
a:hover {
  color: green;
  transition: 0.3s
}
a:not(:hover) {
  transition: 0.3s
}
</style>
