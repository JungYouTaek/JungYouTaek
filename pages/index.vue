<template lang="html">
  <v-carousel icon="remove">
    <v-carousel-item v-for="item in items" v-bind:src="item.src">
      <div>
        <h1>오늘의 식단을 체크해보세요</h1>
        <v-btn class="btn" light flat :router="true" to="/check">검사하기</v-btn>
      </div>
    </v-carousel-item>
  </v-carousel>

</template>

<script>
export default {
  data () {
    return {
      items: [
        { src: 'diet2.jpg' },
        { src: 'diet3.jpg' }
      ]
    }
  }
}
</script>

<style lang="css" scoped>
.carousel__right, .carousel__left {
  display: none;
}
.carousel {
  width: 100%;
  height: 600px;
}
.carousel__item {
  position: relative;
}
.carousel__item:before {
    content:'';
    position: absolute;
    width:100%;
    height:100%;
    top:0;
    left:0;
    background:rgba(0,0,0,0.4);
}
.carousel__item div {
  position: relative;
}
div {
  text-align: center;
}
div .btn {
  border: 2px solid #8BC34A;
  border-radius: 20px;
  width: 200px;
  height: 100px;
  color: white;
}
div .btn:hover {
  background: #8BC34A!important;
  color: white;
  transition: all 0.3s ease!important;
}
div h1 {
  font-size: 50px;
  color: white;
}
@media (max-width: 400px) {
  .carousel {
    width: 100%;
    height: 600px;
  }
}
@media (max-width: 320px) {
  .carousel {
    width: 100%;
    height: 460px;
  }
}
</style>
