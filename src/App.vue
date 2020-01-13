<template>
  <div id="app">
    
    <City/><br>
    <Button/>
    <Heading/>

  </div>

</template>

<script>
import HelloWorld from './components/HelloWorld'
import Heading from './components/Heading'
import City from './components/City'
 import Button from './components/Button'

export default {
  name: 'App',
  components: {
    HelloWorld,
    Heading,
    City,
    Button
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
