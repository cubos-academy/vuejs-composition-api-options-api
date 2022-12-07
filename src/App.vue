<script setup>
import { ref, onMounted } from "vue";

// created my state
const counter = ref(0);

function increment() {
  counter.value++;
}

function decrement() {
  counter.value--;
}

onMounted(() => {
  console.log("onMounted executed...");
});

// export default {
//   data() {
//     return {
//       counter: 0,
//     };
//   },
//   methods: {
//     increment() {
//       this.counter++;
//     },
//     decrement() {
//       this.counter--;
//     },
//   },
//   mounted() {
//     console.log("Mounted ...");
//   },
// };
</script>

<template>
  <div>
    <button @click="decrement()">-</button>
    <h1>{{ counter }}</h1>
    <button @click="increment()">+</button>
  </div>
</template>

<style scoped>
div {
  display: flex;
  gap: 16px;
  align-items: center;
}

button {
  width: 120px;
  height: 48px;

  cursor: pointer;
}
</style>
