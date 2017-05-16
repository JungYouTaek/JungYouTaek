<template lang="html">
  <fade>
  <v-carousel icon="remove">
  <v-carousel-item
    v-for="list in lists"
    v-bind:src="list.picture"
    transition="fade"
    reverseTransition="fade"
  />
  </v-carousel>
</fade>
</template>

<script>
import Vue from 'vue'

Vue.component('fade', {
  function: true,

  render (createElement, context) {
    let data = context.data || {}
    data.props = { name: 'fade' }
    return createElement('transition', data, context.children)
  }
})

export default {
  data () {
    return {
      lists: [
        {picture: '/Slowpoke.png'}
      ]
    }
  }
}
</script>

<style lang="css" scoped>
.fade {
  &-enter-active, &-leave-active, &-leave-to;
    transition: .3s ease-out;
    position: absolute;
    top: 0;
    left: 0
 
  &-enter, &-leave, &-leave-to;
    opacity: 0
}
</style>
