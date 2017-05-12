<template lang="html">
  <v-container>
  <v-stepper v-model="e1">
  <v-stepper-header>
    <v-stepper-step step="1" v-bind:complete="e1 > 1">프로필 입력</v-stepper-step>
    <v-divider />
    <v-stepper-step step="2" v-bind:complete="e1 > 2">식단 입력</v-stepper-step>
    <v-divider />
    <v-stepper-step step="3">결과</v-stepper-step>
  </v-stepper-header>
  <v-stepper-content step="1">
    <v-card class="lighten-1 z-depth-1 mb-5" height="400px">
      <v-card-text>
        <Input-profile/>
      </v-card-text>
    </v-card>
    <v-btn class="light-green" @click.native="e1 = 2">계속</v-btn>
  </v-stepper-content>
  <v-stepper-content step="2">
    <v-card class="lighten-1 z-depth-1 mb-5" height="400px">
      <v-card-text>
        <Input-diet/>
      </v-card-text>
    </v-card>
    <v-btn class="light-green" @click.native="e1 = 3">계속</v-btn>
    <v-btn flat @click.native="e1 = 1">뒤로가기</v-btn>
  </v-stepper-content>
  <v-stepper-content step="3">
    <v-card class="lighten-1 z-depth-1 mb-5" height="400px">
      <v-card-text>
        <div>{{ card_text }}</div>
      </v-card-text>
    </v-card>
    <v-btn class="light-green" @click.native="submit">제출</v-btn>
    <v-btn flat @click.native="e1 = 2">뒤로가기</v-btn>
  </v-stepper-content>
</v-stepper>
</v-container>
</template>

<script>
import InputProfile from '~components/List/InputProfile.vue'
import InputDiet from '~components/List/InputDiet.vue'

export default {
  data () {
    return {
      e1: 1
    }
  },
  components: {
    InputProfile,
    InputDiet
  }
}
</script>

<style lang="css">
.stepper__step--active .stepper__step__step {
  background-color: #8bc34a!important;
}
.stepper__step--complete .stepper__step__step {
  background-color: #8bc34a!important;
}
</style>
