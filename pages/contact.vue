<template lang="html">
  <v-card class="lighten-4 elevation-0">
  <v-card-text>
    <v-container fluid>
      <v-layout row>
       <v-flex xs3 offset-xs1>
         <v-subheader>발신자</v-subheader>
       </v-flex>
       <v-flex xs6>
         <v-text-field
           name="email"
           type="email"
           label="이메일 주소를 입력해주세요"
           class="input-group"
         ></v-text-field>
       </v-flex>
     </v-layout>
      <v-layout row>
       <v-flex xs3 offset-xs1>
         <v-subheader>제목</v-subheader>
       </v-flex>
       <v-flex xs6>
         <v-text-field
           name="title"
           type="text"
           label="제목을 입력해주세요"
           class="input-group"
         ></v-text-field>
       </v-flex>
     </v-layout>
      <v-layout row>
        <v-flex xs3 offset-xs1>
          <v-subheader>내용</v-subheader>
        </v-flex>
        <v-flex xs6>
          <v-text-field
            name="contents"
            type="text"
            label="내용을 입력해주세요"
            class="input-group"
            multi-line
          ></v-text-field>
        </v-flex>
      </v-layout>
        <div class="text-xs-center">
          <v-btn success light>메일 보내기</v-btn>
        </div>
    </v-container>
  </v-card-text>
</v-card>
</template>

<script>
export default {
}
</script>

<style lang="css">
.subheader {
  justify-content: center;
  align-items: flex-end;
}
textarea {
  resize: none;
}
</style>
