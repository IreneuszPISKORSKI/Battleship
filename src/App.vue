<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <BoardOfGame></BoardOfGame>
  </div>
</template>

<script>
import BoardOfGame from "@/components/BoardOfGame";

export default {
  name: 'App',
  components: {
    BoardOfGame
  }
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
