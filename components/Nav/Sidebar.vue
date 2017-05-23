<template>
  <v-navigation-drawer v-model="isActive" temporary>
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
  </v-navigation-drawer>
</template>

<script>
export default {
  data () {
    return {
      isActive: true,
      lists: [
        { header: '메뉴' },
        { avatar: '/home.svg', title: 'Home', subtitle: '홈으로 가기', link: '/' },
        { divider: true, inset: true },
        { avatar: '/check.svg', title: 'Check', subtitle: '검사하기', link: '/check' },
        { divider: true, inset: true },
        { avatar: '/about.svg', title: 'About', subtitle: '페이지 설명', link: '/about' }
      ]
    }
  },
  watch: {
    isActive () {
      this.$store.commit('vuetify/SIDEBAR', this.isActive)
    },
    '$store.state.sidebar' (sidebar) {
      this.isActive = sidebar
    }
  }
}
</script>

<style lang="css">
</style>
