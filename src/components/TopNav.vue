<script setup>
// import { RouterLink, RouterView } from "vue-router";
</script>


/* eslint-disable prettier/prettier */
<template>
  <div class="topnav">
    <router-link to="/"><a class="active" href="#home">Home</a></router-link>
    <a href="#news">News</a>
    <a href="#contact">Contact</a>
    <RouterLink to="/about"><a href="#about">About</a></RouterLink>
  </div>
</template>

<style scoped>
/* Add a black background color to the top navigation */
.topnav {
  background-color: #333;
  overflow: hidden;
}

/* Style the links inside the navigation bar */
.topnav a {
  float: left;
  color: #f2f2f2;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
  font-size: 17px;
}

/* Change the color of links on hover */
.topnav a:hover {
  background-color: #ddd;
  color: black;
}

/* Add a color to the active/current link */
.topnav a.active {
  background-color: #04aa6d;
  color: white;
}
</style>
