<template lang="">
  <div>{{ obj }}</div>
  <div>{{ ddd }}</div>
  <div ref="hahha">heiehei</div>
  <button @click="change">change</button>
</template>
<script setup lang="ts">
import {
  ref,
  reactive,
  shallowRef,
  triggerRef,
  customRef,
  Static,
  onMounted,
} from "vue";
onMounted(() => {
  console.log(hahha.value?.innerText);

});
const obj = shallowRef({ name: "szw", age: 11 });
const hahha = ref<HTMLDivElement>();
const change = () => {
  ddd.value = "7777";
  //   triggerRef(obj);
  console.log(ddd);
};
let ddd = myRef("szw");
function myRef<T>(val: T) {
  let timer: any = null;
  return customRef((track, trigger) => {
    return {
      get() {
        track();
        return val;
      },
      set(newVal: T) {
        clearTimeout(timer);
        timer = setTimeout(() => {
          console.log("hahahah");
          val = newVal;
          trigger();
        }, 500);
      },
    };
  });
}
</script>
<style lang=""></style>
