<template lang="html">
  <v-stepper v-model="e1">
    <v-stepper-header>
      <v-stepper-step step="1" v-bind:complete="e1 > 1">프로필 입력</v-stepper-step>
      <v-divider />
      <v-stepper-step step="2" v-bind:complete="e1 > 2">식단 입력</v-stepper-step>
      <v-divider />
      <v-stepper-step step="3">결과</v-stepper-step>
    </v-stepper-header>
    <v-stepper-content step="1">
      <v-card class="lighten-1 z-depth-1 mb-5" height="450px">
        <v-card-text>
          <Input-profile/>
        </v-card-text>
      </v-card>
      <v-btn class="light-green" @click.native="e1 = 2">계속</v-btn>
    </v-stepper-content>
    <v-stepper-content step="2">
      <v-card class="lighten-1 z-depth-1 mb-5" height="450px">
        <v-card-text>
          <Input-diet/>
        </v-card-text>
      </v-card>
      <v-btn class="light-green" @click.native="e1 = 3">제출</v-btn>
      <v-btn flat @click.native="e1 = 1">뒤로가기</v-btn>
    </v-stepper-content>
    <v-stepper-content step="3">
      <v-card class="lighten-1 z-depth-1 mb-5" height="450px">
        <v-card-text>
          <Result/>
        </v-card-text>
      </v-card>
      <v-btn class="light-green" @click.native="e1 = 1">다시검사하기</v-btn>
    </v-stepper-content>
  </v-stepper>
</template>

<script>
import InputProfile from '~components/List/InputProfile.vue'
import InputDiet from '~components/List/InputDiet.vue'
import Result from '~components/List/Result.vue'

export default {
  data () {
    return {
      e1: 0
    }
  },
  components: {
    InputProfile,
    InputDiet,
    Result
  },
  methods: {
    check: function () {
      // const weight = document.getElementsByName('weight')[0].value
      // if (weight === '') {
      //   alert('몸무게')
      // }
      const gender = document.getElementsByClassName('input-group__selections').firstChild.html()
      if (gender === '') {
        alert('sss')
      }
    }
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
