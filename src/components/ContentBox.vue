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
    max-width: 500px;
  }
}
.content-box {
  /* this hides the weird gap under images */
  /* background-color: #1f1f1f; */
  position: relative;
  width: 100%;
  margin: 10px;
  margin-bottom: 0px;
}
.content-box-img {
  border-top-left-radius: 10px;
  border-top-right-radius: 10px;
  max-width: 100%;
  width: 100%;
  margin-bottom: -5px;
}
.content-box-text {
  display: flex;
  justify-content: center;
  flex-direction: column;

  border-bottom-left-radius: 10px;
  border-bottom-right-radius: 10px;

  text-align: center;
  background-color: #1f1f1f;
  font-size: 25px;
  line-height: 25px;
  font-weight: 500;
  padding: 20px;
  width: 100%;
  
  height: 120px;

  color: #cacaca;
}
</style>
