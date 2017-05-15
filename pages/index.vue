<template lang="html">
  <v-carousel icon="remove">
    <v-carousel-item v-for="(item,i) in items" v-bind:src="item.src" :key="i" />
  </v-carousel>
</template>

<script>
export default {
  data () {
    return {
      items: [
        { src: 'about.svg' },
        { src: 'check.svg' }
      ]
    }
  }
}
</script>

<style lang="css">
  .carousel {
    width: 100%;
    height: 600px;
  }
  @media (max-width: 400px) {
    .carousel {
      width: 100%;
      height: 600px;
    }
  }
  @media (max-width: 320px) {
    .carousel {
      width: 100%;
      height: 460px;
    }
  }
</style>
