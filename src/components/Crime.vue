<template>
  <div>
    <div class="navbar is-dark">Crimes</div>

    <div class="container">{{crime}}</div>
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
    axios.get(`https:///NflArrest.com/api/v1/crime`)
    .then(response => {
      // JSON responses are automatically parsed.
      console.log(response)
      this.crime = response.data
    })
    .catch(e => {
      this.errors.push(e)
    })
    },
    data(){
      return {
        crime: [],
        errors: []
      }
    }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
