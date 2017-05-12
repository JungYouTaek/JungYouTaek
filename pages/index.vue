<template>
  <v-card class="grey lighten-4 elevation-0">
    <v-card-text>
      <v-container fluid>
        <v-row>
          <v-col xs6>
            <v-subheader v-text="'나이'" />
          </v-col>
          <v-col xs6>
            <v-select
              v-bind:items="states"
              v-model="e1"
              label="나이를 선택해 주세요"
              light
              single-line
              auto
            />
          </v-col>
        </v-row>
      </v-container>
    </v-card-text>
  </v-card>
</template>

<script>
export default {
  data () {
    return {
      states: [
        { age: 1 },
        { age: 2 }
      ]
    }
  }
}
</script>

<style lang="css">
</style>
