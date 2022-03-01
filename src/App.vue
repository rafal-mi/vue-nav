<script setup>
import { reactive, computed } from 'vue'
import TopNav from "@/components/TopNav.vue";
import SideNav from "@/components/SideNav.vue";

function sidebar(visible) {
  state.sidebar = visible;
}

const state = reactive({
  sidebar: true,
});
</script>

<template>
  <top-nav @visible="sidebar" />
  <side-nav v-if="state.sidebar" @visible="sidebar" />
  <header>
    <img
      alt="Vue logo"
      class="logo"
      src="@/assets/logo.svg"
      width="125"
      height="125"
    />
  </header>

  <RouterView />
</template>

<style>
@import "@/assets/base.css";
/* @import "@/assets/app.css"; */

</style>
