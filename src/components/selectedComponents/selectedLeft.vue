<template>
  <div>
    <ul class="list">
      <li v-for="item in data" :key="item.id" class="list-item">
        <h3>{{ item.name }}</h3>
      </li>
    </ul>
  </div>
</template>

<script setup>
import { defineProps } from 'vue';
defineProps({
  data: Array,
});
</script>
