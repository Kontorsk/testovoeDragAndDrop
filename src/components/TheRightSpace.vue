<template>
  <div>
    <selectedRight :data="choosedItem" class="selected" />
    <div class="components">
      <ul class="list">
        <li
          @click="$emit('chooseItem', item.id)"
          class="list-item"
          v-for="item in dataRight"
          :key="item.id"
        >
          <h3>{{ item.name }}</h3>
        </li>
      </ul>
    </div>
  </div>
</template>

<script setup>
import selectedRight from './selectedComponents/selectedRight.vue';
import { defineProps, defineEmits } from 'vue';

defineProps({
  dataRight: Array,
  choosedItem: String,
});
defineEmits('chooseItem');
</script>
