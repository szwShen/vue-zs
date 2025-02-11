<template>
  <div>
    {{ a }}
  </div>
  <button @click="add">add</button>
</template>
<script setup lang="ts">
import { ref } from "vue";
let a = ref(0);
const add = () => {
    a.value++
};
</script>
<style lang="" scoped></style>
