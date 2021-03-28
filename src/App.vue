<template>
  <div id="app">
    <h1>The Impractical Bar</h1>
    <p><i>Coming {{ randomDate }}</i></p>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld
  },
  computed: {
    randomDate: function () {
      let start = new Date(Date.now());
      let dayOffset = Math.random() * 7;
      let date = new Date(start.getFullYear(), start.getMonth(), start.getDate() + dayOffset);
      let months = ["January", "Feburary", "March", "April", "May", "June", "July", "August", "September", "October", "November", "December"];
      let monthName = months[date.getMonth()];
      return monthName + " " + date.getDate();
    }
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
