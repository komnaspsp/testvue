<template>
<div class="container">

<Card>
<Header/>
</Card>
</div>

 
</template>

<script>
 /* eslint-disable */
import Card from "./components/Card.vue"
import Header from"./components/header.vue"


export default {

 
  components: {
    Card,
    Header
  
    
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
