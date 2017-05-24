<template lang="html">
  <v-card class="lighten-4 elevation-0">
    <v-card-text>
      <v-container fluid>
        <v-layout row wrap>
          <v-flex xs6>
            <v-subheader>성별</v-subheader>
          </v-flex>
          <v-flex xs6>
            <v-select
              v-bind:items="gender"
              v-model="e1"
              label="성별"
              dark
              single-line
              auto
            ></v-select>
          </v-flex>
          <v-flex xs6>
            <v-subheader>연령대</v-subheader>
          </v-flex>
          <v-flex xs6>
            <v-select
              v-bind:items="age"
              v-model="e1"
              label="나이"
              dark
              single-line
              auto
            ></v-select>
          </v-flex>
          <v-flex xs6>
            <v-subheader>일일 활동량</v-subheader>
          </v-flex>
          <v-flex xs6>
            <v-select
              v-bind:items="activity"
              v-model="e1"
              label="일일 활동량"
              dark
              single-line
              auto
            ></v-select>
          </v-flex>
          <v-flex xs4>
            <v-subheader>몸무게</v-subheader>
          </v-flex>
          <v-flex xs8>
            <v-text-field
              name="weight"
              label="몸무게"
            ></v-text-field>
          </v-flex>
        </v-layout>
      </v-container>
    </v-card-text>
  </v-card>
</template>

<script>
export default {
  data () {
    return {
      gender: ['남자', '여자'],
      age: ['18세 이하', '18세~30세', '30세~60세', '60세 이상'],
      activity: ['매우적음', '적음', '보통', '많음', '매우많음']
    }
  }
}
</script>

<style lang="css">
</style>
