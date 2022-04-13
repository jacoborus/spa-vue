<script setup lang="ts">
import { ref } from "vue";

const props = defineProps<{
  initial: number;
}>();

const count = ref(props.initial);
const inc = () => count.value++;
const dec = () => count.value--;
</script>

<template>
  <div>
    {{ count }}
    <button class="inc" @click="inc()">+</button>
    <button class="dec" @click="dec()">-</button>
  </div>
</template>
