<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <Team/>
    <Player/>
    <Position/>
    <Crime/>
  </div>
</template>

<script>
import Team from './components/Team.vue'
import Player from './components/Players.vue'
import Position from './components/Positions.vue'
import Crime from './components/Crime.vue'

export default {
  name: 'app',
  components: {
    Team,
    Player,
    Position,
    Crime
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
