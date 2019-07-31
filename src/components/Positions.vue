<template>
  <div>
    <div class="navbar is-dark">Positions</div>

    <div class="container">{{positions}}</div>
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
    axios.get(`http:///NflArrest.com/api/v1/position`)
    .then(response => {
      // JSON responses are automatically parsed.
      console.log(response)
      this.positions = response.data
    })
    .catch(e => {
      this.errors.push(e)
    })
    },
    data(){
      return {
        positions: [],
        errors: []
      }
    }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
