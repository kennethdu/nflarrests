<template>
  <div>
    <div class="navbar is-dark">Players</div>

    <div class="container">{{players}}</div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
  mounted() {
    axios.get(`http:///NflArrest.com/api/v1/player`)
    .then(response => {
      // JSON responses are automatically parsed.
      console.log(response)
      this.players = response.data
    })
    .catch(e => {
      this.errors.push(e)
    })
    },
    data(){
      return {
        players: [],
        errors: []
      }
    }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
