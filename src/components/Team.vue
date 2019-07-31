<template>
  <div>
    <div class="navbar is-dark">Teams</div>

    <div class="container">{{posts}}</div>
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
    axios.get(`https:///NflArrest.com/api/v1/team`)
    .then(response => {
      // JSON responses are automatically parsed.
      console.log(response)
      this.posts = response.data
    })
    .catch(e => {
      this.errors.push(e)
    })
    },
    data(){
      return {
        posts: [],
        errors: []
      }
    }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
