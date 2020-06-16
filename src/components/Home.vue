<template>
  <div class="container">
    <h1 class="orange-shadow" style="font-size: 4vw">Plasma</h1>
    <h3 class="orange-shadow">The free IOT search engine</h3>
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

.orange-shadow {
  text-shadow: 3px 3px #000000;
  font-size: 3vw;
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

</style>
