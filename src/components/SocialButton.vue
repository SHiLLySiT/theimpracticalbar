<template>
  <span class="social-button" @click="onClick">
    <font-awesome-icon size="lg" :icon="iconArray" />
  </span>
</template>

<script>
export default {
  name: 'SocialButton',
  props: {
    icon: String,
  },
  computed: {
    iconArray: function() {
      return ['fab', this.icon];
    }
  },
  methods: {
    onClick: function() {
      window.open("https://www.youtube.com/watch?v=dQw4w9WgXcQ&ab_channel=RickAstleyVEVO");
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.social-button {
  cursor: pointer; 
}
</style>
