<template>
  <div id="app">
    <div id="container">
      <div id="header">
        <img src="./assets/logo.svg" />
      </div>
      
      <div id="bar-photo">
        <img src="./assets/placeholder-bar.jpg" />
      </div>

      <div class="content-box" id="about">
        <h2>ABOUT</h2>
        <p>Inconveniently located at {{ randomAddress }}. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas auctor eget magna et rhoncus. Duis fermentum eros sit amet turpis condimentum, sit amet scelerisque dui scelerisque. Nam ac accumsan diam, sit amet rhoncus justo.</p>
      </div>

      <div class="content-box" id="menu">
        <h2>DRINKS</h2>
        <p>Proin sagittis, justo nec mollis feugiat, metus nisi imperdiet tellus, ut aliquam velit justo fermentum nunc. Nam cursus sapien ac lectus ullamcorper finibus. Nullam vel posuere risus, id tincidunt velit. Maecenas sollicitudin leo odio. Integer nec eros diam.</p>
      </div>

      <div class="content-box" id="contact">
        <h2>CONTACT</h2>
        <p>Please fax {{ randomNumber }} for reservations</p>
        <p>Donec mauris est, suscipit viverra molestie sed, interdum vel lacus. Mauris elementum cursus tortor, in ultricies neque aliquam imperdiet. </p>
      </div>

    </div>
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
    },
    randomAddress: function () {
      // TODO
      return "1234 Bar Way";
    },
    randomNumber: function () {
      // TODO
      return "(123) 456-7890";
    }
  },
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Suranna&display=swap');

body {
  margin: 0px;
}

#app {
  font-family: 'Suranna', serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #111111;
}

#container {
  display: flex;
  flex-direction: column;
}

#header {
  display: flex;
  padding: 25px;
}

/* #about {
  padding: 50px 25px;
} */
p { 
  font-size: 20px;
  font-weight: 500;
}
#menu {
  background-color: #F7EFE3;
}

.content-box {
  padding: 25px 25px;
  /* border: red 1px solid; */
}

h2 {
  
}

img {
  max-width: 100%;
  max-height: 100%;
}
</style>
