<template lang="html">
  <v-tabs
    id="mobile-tabs-1"
    grow
    scroll-bars
    v-model="active"
    light
  >
    <v-tabs-bar slot="activators">
      <v-tabs-item
        v-for="food in foods"
        :key="food.id"
        :href="'#mobile-tabs-1-' + food.id"
        ripple
      >
        {{ food.name }}
      </v-tabs-item>
      <v-tabs-slider></v-tabs-slider>
    </v-tabs-bar>
    <v-tabs-content
      v-for="food in foods"
      :key="food.id"
      :id="'mobile-tabs-1-' + food.id"
    >
      <v-card flat>
        <v-card-text>{{ food.option }}</v-card-text>
      </v-card>
    </v-tabs-content>
  </v-tabs>
</template>

<script>
export default {
  data () {
    return {
      active: null,
      foods: [
        { id: 1, name: '밥', option: '하이' },
        { id: 2, name: '빵', option: '헬로' }
      ]
    }
  }
}
</script>

<style lang="css">
.tabs ul {
  background-color: #8bc34a!important;
}
</style>
