<template>
  <div>
    <div class="topnav" id="nav">
      <router-link to="/">Home</router-link>
      <router-link to="/explore">Explore</router-link>
      <a href="">API</a>
      <router-link to="/contact">Contact</router-link>
      <router-link to="/about">About</router-link>
      <a href="javascript:void(0);" class="icon" v-on:click="navClick">
        <i class="fas fa-bars"></i>
      </a>
      <div class="search-container">
        <input v-model="term" @keyup.enter="$router.push({ path: 'search', query: { term: term } })" type="text" placeholder="Search">
        <button @click="$router.push({ path: 'search', query: { term: term } })"><i class="fas fa-search"></i></button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Navbar',
  data () {
    return {
      term: null
    }
  },
  methods: {
    navClick: () => {
      let x = document.getElementById('nav')
      if (x.className === 'topnav') {
        x.className += ' responsive'
      } else {
        x.className = 'topnav'
      }
    }
  }
}
</script>

<style scoped>

.topnav {
  overflow: hidden;
  background-color: #000;
  box-shadow: 8px 0px 8px 8px rgba(0,0,0,0.4);
}

.topnav a {
  float: left;
  display: block;
  color: #f2f2f2;
  text-align: center;
  padding: 18px 20px;
  text-decoration: none;
  font-size: 17px;
  transition-duration: 0.3s;
  border-bottom: transparent 3px solid;
}

.topnav a:hover {
  border-bottom: 3px solid rgb(0, 148, 247);
}

.topnav .icon {
  display: none;
}

.search-container {
  float: right;
}

.topnav input[type=text] {
  background-color: transparent;
  color: #ffffff;
  padding: 6px;
  margin-top: 11px;
  font-size: 17px;
  border: 2px solid #ffffff;
  border-top-left-radius: 5px;
  border-bottom-left-radius: 5px;
}

.topnav input[type=text]:focus, button {
   outline-width: 0;
}

.topnav .search-container button {
  transition-duration: 0.3s;
  color: #ffffff;
  height: 37px;
  float: right;
  padding: 6px;
  margin-top: 11px;
  margin-right: 25px;
  background-color: rgb(202, 0, 202);
  font-size: 17px;
  border: none;
  cursor: pointer;
  border-top-right-radius: 5px;
  border-bottom-right-radius: 5px;
}

.topnav .search-container button:hover {
  background: rgb(0, 148, 247);
}

@media screen and (max-width: 912px) {
  .topnav a:not(:first-child) {display: none;}
  .search-container {display: none;}
  .topnav a.icon {
    float: right;
    display: block;
  }
  .topnav a {border: none;}
  .topnav a:hover {
    border: none;
    background-color: teal;
  }
}

@media screen and (max-width: 912px) {
  .topnav.responsive {position: relative;}
  .topnav.responsive .icon {
    position: absolute;
    right: 0;
    top: 0;
  }
  .topnav.responsive a {
    float: none;
    display: block;
    text-align: left;
  }
  .search-container {
    float: left;
  }
}
</style>
