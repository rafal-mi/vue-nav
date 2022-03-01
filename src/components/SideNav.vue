<template>
  <div class="sidenav">
    <a
      href="javascript:void(0)"
      class="closebtn"
      @click="$emit('visible', false)"
      >&times;</a
    >
    <router-link to="/" class="active item">Home</router-link>
    <router-link to="/about" class="item">About</router-link>
  </div>
</template>

<style scoped>
.sidenav {
  height: 100%;
  width: 33%;
  position: fixed;
  z-index: 1;
  top: 0;
  left: 0;
  background-color: #111;
  overflow-x: hidden;
  transition: 1.0s;
  padding-top: 60px;
}

.sidenav a {
  padding: 8px 8px 8px 32px;
  text-decoration: none;
  font-size: 25px;
  color: #818181;
  display: block;
  transition: 0.3s;
}

.sidenav a:hover {
  color: #f1f1f1;
}

.sidenav .closebtn {
  position: absolute;
  top: 0;
  right: 25px;
  font-size: 36px;
  margin-left: 50px;
}

@media screen and (max-height: 450px) {
  .sidenav {padding-top: 15px;}
  .sidenav a {font-size: 18px;}
}

</style>