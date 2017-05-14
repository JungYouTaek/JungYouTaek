<template lang="html">
  <v-card class="lighten-4 elevation-0">
  <v-card-text>
    <v-container fluid>
      <v-row row>
       <v-col xs2 offset-xs2>
         <v-subheader>발신자</v-subheader>
       </v-col>
       <v-col xs6>
         <v-text-field
           name="email"
           label="이메일 주소를 입력해주세요"
           class="input-group"
         ></v-text-field>
       </v-col>
     </v-row>
      <v-row row>
       <v-col xs2 offset-xs2>
         <v-subheader>제목</v-subheader>
       </v-col>
       <v-col xs6>
         <v-text-field
           name="title"
           label="제목을 입력해주세요"
           class="input-group"
         ></v-text-field>
       </v-col>
     </v-row>
      <v-row row>
        <v-col xs2 offset-xs2>
          <v-subheader>내용</v-subheader>
        </v-col>
        <v-col xs6>
          <v-text-field
            name="contents"
            label="내용을 입력해주세요"
            class="input-group"
            multi-line
          ></v-text-field>
        </v-col>
      </v-row>
      <v-row row>
        <v-col xs2 offset-xs8>
          <v-btn light default>메일 보내기</v-btn>
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
.subheader {
  justify-content: center;
  align-items: flex-end;
}
textarea {
  resize: none;
}
</style>
