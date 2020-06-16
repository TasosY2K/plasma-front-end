<template>
  <div id="app">
    <Navbar/>
    <router-view/>
  </div>
</template>

<script>
import Navbar from '@/components/Navbar'
export default {
  name: 'App',
  components: {
    'Navbar': Navbar
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Krona+One&display=swap');

html, body {
    height: 100%;
}

body {
  margin: 0;
  font-family: 'Krona One', sans-serif;
  background-color: #FF3CAC;
  background-image: linear-gradient(225deg, #FF3CAC 0%, #784BA0 50%, #2B86C5 100%);
  background-attachment: fixed;
}

input, textarea, select, button { font-family:inherit; }

#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
</style>
