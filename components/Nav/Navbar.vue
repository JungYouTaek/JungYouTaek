<template>
  <nav id="gnb" fixed>
    <v-toolbar class="light-green">
      <v-toolbar-side-icon @click.native.stop="$store.commit('vuetify/SIDEBAR', true)" />
      <v-toolbar-title><a href="/">영양만점</a></v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-item href="https://github.com/JungYouTaek/nuxt-practice" ripple><img src="/github.svg" alt="github-logo"></v-toolbar-item>
      <v-toolbar-item href="/contact" ripple><img src="/speech-bubble.svg" alt="contact us"></v-toolbar-item>
      <v-menu bottom right>
        <v-btn icon="icon" slot="activator" dark>
          <v-icon>more_vert</v-icon>
        </v-btn>
        <v-list>
          <v-list-item v-for="item in items" :key="item">
            <v-list-tile>
              <v-list-tile-title>{{ item.title }}</v-list-tile-title>
            </v-list-tile>
          </v-list-item>
        </v-list>
      </v-menu>
    </v-toolbar>
  </nav>
</template>

<script>
export default {
  data () {
    return {
      items: [
        { title: '회원가입' },
        { title: '개인정보' }
      ]
    }
  }
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
.list__tile__title {
  color: #8bc34a;
}
.list__item a:hover {
  color: green;
}
</style>
