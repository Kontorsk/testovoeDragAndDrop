<template>
  <div>
    <selectedLeft :data="selectedArray" class="selected" />
    <div class="components">
      <ul class="list">
        <li
          @click="$emit('selectItem', item.id)"
          class="list-item"
          v-for="item in dataLeft"
          :key="item.id"
        >
          <h3>{{ item.name }}</h3>
        </li>
      </ul>
    </div>
  </div>
</template>

<script setup>
import selectedLeft from './selectedComponents/selectedLeft.vue';
import { defineProps, defineEmits } from 'vue';

defineProps({
  dataLeft: Array,
  selectedArray: Array,
});
defineEmits('selectItem');
</script>
