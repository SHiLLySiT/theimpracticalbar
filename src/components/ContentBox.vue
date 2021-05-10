<template>
  <div class="content-box">
      <img class="content-box-img" :src="require('../assets/' + imageName + '.jpg')" />
      <div class="content-box-text">
        {{ content }}
      </div>
  </div>
</template>

<script>
export default {
  name: 'ContentBox',
  props: {
    imageName: String,
    content: String,
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
@media screen and (min-width: 1260px) {
  .content-box {
    max-width: 600px;
  }
}
.content-box {
  /* this hides the weird gap under images */
  /* background-color: #1f1f1f; */
  position: relative;
  width: 100%;
}
.content-box-img {
  max-width: 100%;
  width: 100%;
}

@media screen and (min-width: 1260px) {
  .content-box-text {
    font-size: 50px;
    line-height: 50px;
  }
}
.content-box-text {
  text-align: center;
  /* background-color: #1f1f1f; */
  background-image: linear-gradient(rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.7) 30%,  rgba(0, 0, 0, .9));
  font-size: 25px;
  line-height: 25px;
  font-weight: 500;
  padding: 20px;
  width: 100%;
  
  position: absolute;
  bottom: 0px;
  left: 0px;

  color: #cacaca;
}
</style>
