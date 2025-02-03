<template>
  <div>
    <selectedLeft :data="selectedArray" class="selected" />
    <div class="components">
      <draggable :list="dataLeft" tag="ul" group="data" class="list">
        <template #item="item">
          <li @click="$emit('selectItem', item.element.id)" class="list-item">
            <h3>{{ item.element.name }}</h3>
          </li>
        </template>
      </draggable>
    </div>
  </div>
</template>

<script setup>
import selectedLeft from './selectedComponents/selectedLeft.vue';
import { defineProps, defineEmits } from 'vue';
import draggable from 'vuedraggable';

defineProps({
  dataLeft: Array,
  selectedArray: Array,
});
defineEmits('selectItem');
</script>
