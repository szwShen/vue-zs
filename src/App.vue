<script setup lang="ts">
import Hello3 from './components/Hello3.vue';
import Hello4 from './components/Hello4.vue';
import HelloWorld from './components/HelloWorld.vue'
import HelloWorld2 from './components/HelloWorld2.vue'
</script>

<template>
 <div>
  <!-- <HelloWorld2></HelloWorld2>
  <HelloWorld msg="Vite + Vue" /> -->
  <!-- <Hello3></Hello3> -->
   <Hello4></Hello4>
 </div>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
