<template>
  <nav id="gnb" fixed>
    <v-toolbar class="light-green">
      <v-toolbar-side-icon @click.native.stop="$store.commit('vuetify/SIDEBAR', true)" />
      <v-toolbar-title><a href="/">영양만점</a></v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-item href="https://github.com/JungYouTaek/nuxt-practice" ripple><img src="/github.svg" alt="github-logo"></v-toolbar-item>
      <v-toolbar-item href="/contact" ripple><img src="/speech-bubble.svg" alt="contact us"></v-toolbar-item>
      <v-toolbar-item ripple>Link</v-toolbar-item>
    </v-toolbar>
  </nav>
</template>

<script>
export default {
  data () {
    return {
      sidebar: false,
      lists: [
        { header: '메뉴' },
        { avatar: '/home.svg', title: 'Home', subtitle: '홈으로 가기', link: '/Home' },
        { divider: true, inset: true },
        { avatar: '/check.svg', title: 'Check', subtitle: '검사하기', link: '/check' },
        { divider: true, inset: true },
        { avatar: '/about.svg', title: 'About', subtitle: '페이지 설명', link: '/about' }
      ]
    }
  }
=======
>>>>>>> ef62200810fb793f588bd02a19a66ce034b2c754
}
</script>

<style lang="css" scoped>
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
li {
  list-style: none;
}
</style>
