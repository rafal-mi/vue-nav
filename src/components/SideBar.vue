<template>
  <div
    class="w3-sidebar w3-bar-block w3-border-right w3-animate-left w3-animate-opacity"
    style="display: block"
    id="mySidebar"
  >
    <button @click="$emit('visible', false)" class="w3-bar-item w3-large">
      Close &times;
    </button>
    <a href="#" class="w3-bar-item w3-button">Link 1</a>
    <a href="#" class="w3-bar-item w3-button">Link 2</a>
    <a href="#" class="w3-bar-item w3-button">Link 3</a>
  </div>
</template>
