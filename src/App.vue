<script setup>
import { reactive, computed } from 'vue'
import TopNav from "@/components/TopNav.vue";
import TopBar from "@/components/TopBar.vue";
import SideNav from "@/components/SideNav.vue";
import SideBar from "@/components/SideBar.vue";

function visibility(visible) {
  state.visible = visible;
}

const state = reactive({
  visible: false,
});
</script>

<template>
  <!-- <top-nav @visible="sidebar" /> -->
  <top-bar @visible="visibility" />

  <!-- <Transition name="slide-fade">
    <side-nav class="sidenav" v-if="state.sidebar" @visible="sidebar" />
  </Transition> -->
  <side-bar class="sidebar" v-if="state.visible" @visible="visibility" />

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
@import "@/assets/w3.css";
@import "@/assets/base.css";
/* @import "@/assets/app.css"; */

.sidenav {
  width: 500px;
  transform: translateX(0px);
}

.slide-fade-enter-active {
  transition: all 0.3s ease-out;
}

.slide-fade-leave-active {
  transition: all 0.8s cubic-bezier(1, 0.5, 0.8, 1);
}

.slide-fade-enter-to,
.slide-fade-leave-from {
  transform: translateX(0px);
  opacity: 1.0;
}

.slide-fade-enter-from,
.slide-fade-leave-to {
  transform: translateX(-500px);
  opacity: 0;
}

/* Side Bar */

.sidebar {
  position: fixed;
  top: 0;
  left: 0;
}

</style>
