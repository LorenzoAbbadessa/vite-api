<script>
import axios from 'axios'

export default {
  data() {
    return {
      search: ""
    }
  },
  mounted() {
    axios.get("https://api.openbrewerydb.org/v1/breweries?by_country=austria&per_page=10").then(result => {
      console.log(result)
    })
  }
}
</script>


<template>
  <h1>BIRRERIE</h1>
  <input type="text" placeholder="Cerca il tuo Bar"> <br> <br>
  <button>INVIA</button>
</template>


<style>
body {
  display: flex;
  justify-content: center;

}
</style>