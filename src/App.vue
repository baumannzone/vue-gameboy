<template>
  <GameBoy />
</template>

<script>
import GameBoy from "./components/GameBoy.vue";

export default {
  name: "App",
  components: {
    GameBoy,
  },
};
</script>

<style lang="stylus">
#app
  font-family Avenir, Helvetica, Arial, sans-serif
  -webkit-font-smoothing antialiased
  -moz-osx-font-smoothing grayscale
  margin-top 60px
</style>
