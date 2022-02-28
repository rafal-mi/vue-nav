<script setup>
import { RouterLink, RouterView } from "vue-router";
import TopNav from "@/components/TopNav.vue";

</script>

<template>
  <TopNav />
  <header>
    <img
      alt="Vue logo"
      class="logo"
      src="@/assets/logo.svg"
      width="125"
      height="125"
    />

    <div class="wrapper">
      <HelloWorld msg="You did it!" />

      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
    </div>
  </header>

  <RouterView />
</template>

<style>
@import "@/assets/base.css";
/* @import "@/assets/app.css"; */

</style>
