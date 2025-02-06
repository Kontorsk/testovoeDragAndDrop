<template>
  <div>
    <h1 class="item">{{ data }}</h1>
  </div>
</template>

<script setup>
import { defineProps } from 'vue';

defineProps({
  data: {
    type: String,
    required: true,
  },
});
</script>

<style scoped>
.selected {
  margin-left: 250px;
}
.item {
  text-align: center;
  font-size: 64px;
  margin-top: 90px;
}
</style>
