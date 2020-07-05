<template>
  <div class="container">
    <h1 class="header1 center">Plasma</h1>
    <h3 class="header1">The free IOT search engine</h3>
    <p>Discover devices from all around the world and witness<br> the beauty of 21st century's interconnectedness firsthand</p>
    <p>Straigh forward and easy to use interface</p>
    <p style="margin-bottom: 70px">No sign up. No fees. 100% Open source</p>
    <router-link to="/explore" class="explore-btn fill">Explore IOT Devices</router-link>
  </div>
</template>

<script>
export default {
  name: 'Home'
}
</script>

<style scoped>
.container {
  color: #ffffff;
  margin: 0 10vw;
  margin-top: 5%;
}

.header1 {
  text-shadow: 3px 3px #000000;
  font-size: 3.5vw;
}

.explore-btn {
  border: none;
  background-color: #000000;
  text-decoration: none;
  color: #ffffff !important;
  font-weight: 100;
  padding: 20px;
  text-transform: uppercase;
  border-radius: 6px;
  display: inline-block;
  transition: all 0.3s ease 0s;
}

.explore-btn:hover {
  color: #ffffff !important;
  font-weight: 700 !important;
  letter-spacing: 3px;
  background-color: rgb(202, 0, 202);
  box-shadow: 0px 5px 40px -10px rgba(0,0,0,0.57);
  -webkit-box-shadow: 0px 5px 40px -10px rgba(0,0,0,0.57);
  -moz-box-shadow: 0px 5px 40px -10px rgba(0,0,0,0.57);
  transition: all 0.3s ease 0s;
}

@media screen and (max-width: 500px) {
  .header1 {
    font-size: 6vw;
  }
}
</style>
