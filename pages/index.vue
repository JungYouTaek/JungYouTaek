<template lang="html">
<<<<<<< HEAD
  <Home/>
=======
  <v-carousel icon="remove">
    <v-carousel-item v-for="(item,i) in items" v-bind:src="item.src" :key="i" />
  </v-carousel>
>>>>>>> ef62200810fb793f588bd02a19a66ce034b2c754
</template>

<script>
import Home from '~components/List/Home.vue'

export default {
<<<<<<< HEAD
  components: {
    Home
=======
  data () {
    return {
      items: [
        { src: 'about.svg' },
        { src: 'check.svg' }
      ]
    }
>>>>>>> ef62200810fb793f588bd02a19a66ce034b2c754
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
