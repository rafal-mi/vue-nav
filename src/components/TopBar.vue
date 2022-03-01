<script setup>
// import { RouterLink, RouterView } from "vue-router";
</script>


/* eslint-disable prettier/prettier */
<template>
  <div class="w3-bar w3-black">
    <router-link to="/" class="w3-bar-item w3-button">Home</router-link>
    <router-link to="/about" class="w3-bar-item w3-button">About</router-link>
    <div class="w3-bar-item w3-button w3-right" @click="$emit('visible', true)">&#9776;</div>
  </div>
</template>

<style scoped>
/* Add a black background color to the top navigation */
.topnav {
  background-color: #333;
  overflow: hidden;
}

/* Style the links inside the navigation bar */
.item {
  float: left;
  color: #f2f2f2;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
  font-size: 17px;
}

.item.item-right {
  float: right;
}

.item-right:hover {
  cursor: pointer;
}

/* Change the color of links on hover */
.topnav .item:hover {
  background-color: #ddd;
  color: black;
}

/* Add a color to the active/current link */
.topnav a.active {
  background-color: #04aa6d;
  color: white;
}
</style>
