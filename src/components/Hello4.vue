<template>
  <!-- <div>{{ obj }}</div>
  <div>{{ obj2 }}</div> -->
  <button @click="change">change</button>
  <ul>
    <li v-for="item in arr.list">
      {{ item }}
    </li>
  </ul>
</template>
<script setup lang="ts">
import { reactive, shallowReactive, readonly } from "vue";
// const obj: any = reactive({
//   bar: {
//     fool: {
//       age: 18,

//       name: "szw",
//     },
//   },
// });
// const obj2: any = shallowReactive({
//   bar: {
//     fool: {
//       name: "szw",
//     },
//   },
// });
type Person = {
  list?: Array<String>;
};
const arr = reactive<Person>({ list: [] });
const change = () => {
  var newArr = ["1", "2", "4"];
  setTimeout(() => {
    arr.list = newArr;
  }, 2000);
  //   console.log(obj2);
  //   obj.bar.fool.name = "szw2";
  //   obj2.bar.fool.name = "wo 的心智";
};
</script>
<style lang=""></style>
