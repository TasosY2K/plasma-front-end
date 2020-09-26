<template>
    <div>
        <h1 class="header" style="color: #fff">Explore Over <span class="blue">{{ info.length - 1 }}</span> Devices</h1>
        <div class="explore-container">
            <div class="card" v-for="i in info" :key="i.id">
                <img v-bind:src="'http://localhost/devices/img/' + i.id">
                <div class="container">
                    <h3>{{ i.title }}</h3>
                    <p><a class="ip-link" target="_blank" v-bind:href="'http://' + i.ip_address">{{ i.ip_address }}</a>&nbsp;&nbsp;<span class="status">{{ i.status_code }}</span></p>
                    <p><img class="country-img" v-bind:src="'https://www.countryflags.io/' + i.country.toLowerCase() + '/flat/64.png'"> {{ i.region }}, {{ i.city }}</p>
                    <p>{{ i.isp }}</p>
                    <p><i>{{ i.time_located }}</i></p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import axios from 'axios'
export default {
  name: 'Explore',
  data () {
    return {
      info: null
    }
  },
  mounted () {
    axios
      .get('http://localhost/devices')
      .then(response => (this.info = response.data.reverse()))
  }
}
</script>

<style scoped>
.card {
  color: black;
  text-align: left;
  box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
  transition: 0.3s;
  width: 90%;
  margin: 20px;
  border-radius: 10px;
  background-color: #ffffff;
}

.card img {
  width: 100%;
  height: auto;
  border-radius: 10px;
  object-fit: cover;
}

.card:hover {
  box-shadow: 0px 8px 8px 0 rgba(0,0,0,0.4);
  transform: translateY(-5px);
}

.explore-container {
  display: grid;
  align-items: center;
  grid-template-columns: repeat(auto-fill, minmax(390px, 1fr));
}

.container {
    padding: 0 10px;
}

.country-img {
    height: 24px !important;
    width: 24px !important;
    vertical-align: bottom !important;
}

.ip-link {
    color: #000000;
    text-decoration: none;
    transition: 0.1s;
}

.ip-link:hover {
    border-bottom: 1.5px solid rgb(114, 114, 114);
}

.status {
    background-color: rgb(0, 148, 0);
    color: #ffffff;
    padding: 2px;
    border-radius: 5px;
}
</style>
