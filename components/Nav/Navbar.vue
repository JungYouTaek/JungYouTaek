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
      <v-list two-line>
        <template v-for="list in lists.slice(0, 6)">
          <v-subheader v-if="list.header" v-text="list.header" />
          <v-divider v-else-if="list.divider" v-bind:inset="list.inset" />
          <v-list-item v-else v-bind:key="list.title">
            <v-list-tile avatar :href="list.link">
              <v-list-tile-avatar>
                <img v-bind:src="list.avatar" />
              </v-list-tile-avatar>
              <v-list-tile-content>
                <v-list-tile-title v-html="list.title" />
                <v-list-tile-sub-title v-html="list.subtitle" />
              </v-list-tile-content>
            </v-list-tile>
          </v-list-item>
        </template>
      </v-list>
    </v-sidebar>
  </nav>
</template>

<script>
export default {
  data () {
    return {
      sidebar: false,
      lists: [
        { header: '메뉴' },
        { avatar: '/home.svg', title: 'Home', subtitle: '홈으로 가기', link: '/' },
        { divider: true, inset: true },
        { avatar: '/check.svg', title: 'Check', subtitle: '검사하기' },
        { divider: true, inset: true },
        { avatar: '/about.svg', title: 'About', subtitle: '페이지 설명', link: '/about' }
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
