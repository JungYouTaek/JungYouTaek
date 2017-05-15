<template lang="html">
  <v-tabs id="mobile-tabs-3" centered scroll-bars>
    <v-tab-item
      v-for="food in foods" :key="food.id"
      v-bind:href="'#mobile-tabs-3-' + food.id"
      slot="activators"
    >
      {{ food.name }}
    </v-tab-item>
    <v-tab-content
      v-for="food in foods" :key="food.id"
      v-bind:id="'mobile-tabs-3-' + food.id"
      slot="content"
    >
      <v-card>
        <v-card-text>{{ food.option }}</v-card-text>
      </v-card>
    </v-tab-content>
  </v-tabs>
</template>

<script>
export default {
  data () {
    return {
      foods: [
        { id: 1, name: '밥', option: 'menu' },
        { id: 2, name: '빵', option: 'menu2' }
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
