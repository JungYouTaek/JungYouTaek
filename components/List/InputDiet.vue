<template lang="html">
  <v-card class="lighten-4 elevation-0">
  <v-card-text>
    <v-container fluid>
      <v-row>
        <v-col xs6>
          <v-subheader v-text="'Standard'" />
        </v-col>
        <v-col xs6>
          <v-select
            v-bind:items="states"
            v-model="e1"
            label="Select"
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
}
</script>

<style lang="css">
</style>
