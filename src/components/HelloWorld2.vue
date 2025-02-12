<template>
  <div><!-- {{ message.split(",") }} -->{{ a }}</div>
  <!-- <div :class="['aa', 'bb']">szw</div>
  <div :class="[a ? 'aa' : 'bb']">szw</div>
  <div :style="obj">szw</div> -->
  <div :class="[obj, 'h']">{{ message }}</div>
  <input type="text" v-model="message" />
  <!-- <button @click="add">add</button> -->
</template>
<script setup lang="ts">
import { ref } from "vue";
let a = ref(0);
const message = ref("woshidaman");
type Flag = {
  aa: boolean;
  bb: boolean;
};
const obj: Flag = {
  aa: true,
  bb: false,
};
const add = () => {
  a.value++;
};
</script>
<style lang="css" scoped>
.aa {
  color: red;
}
.bb {
  border: 1px solid;
}
.h {
  font-size: 30px;
}
</style>
