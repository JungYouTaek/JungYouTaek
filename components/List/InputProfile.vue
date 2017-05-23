<template lang="html">
  <v-card class="lighten-4 elevation-0">
    <v-card-text>
      <v-container fluid>
        <v-row>
          <v-col xs6>
            <v-subheader v-text="'성별'" />
          </v-col>
          <v-col xs6>
            <v-select
            v-bind:items="gender"
            label="성별"
            name="gender"
            light
            single-line
            auto
            />
          </v-col>
          <v-col xs6>
            <v-subheader v-text="'연령대'" />
          </v-col>
          <v-col xs6>
            <v-select
            v-bind:items="age"
            label="연령대"
            name="age"
            light
            single-line
            auto
            />
          </v-col>
          <v-col xs6>
            <v-subheader v-text="'일일 활동량'" />
          </v-col>
          <v-col xs6>
            <v-select
            v-bind:items="activity"
            label="일일 활동량"
            name="activity"
            light
            single-line
            auto
            />
          </v-col>
          <v-col xs6>
            <v-subheader v-text="'몸무게'"></v-subheader>
          </v-col>
          <v-col xs6>
            <v-text-field
            type="number"
            name="weight"
            label="몸무게(숫자만)"
            ></v-text-field>
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
      gender: ['남자', '여자'],
      age: ['18세 이하', '18세~30세', '30세~60세', '60세 이상'],
      activity: ['매우적음', '적음', '보통', '많음', '매우많음']
    }
  }
}
</script>

<style lang="css">
</style>
