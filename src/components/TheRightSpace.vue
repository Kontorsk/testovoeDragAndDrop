<template>
  <div>
    <selectedRight :data="choosedItem" class="selected" />
    <div class="components">
      <draggable :list="dataRight" tag="ul" group="data" class="list">
        <template #item="item">
          <li @click="$emit('chooseItem', item.element.id)" class="list-item">
            <h3>{{ item.element.name }}</h3>
          </li>
        </template>
      </draggable>
    </div>
  </div>
</template>

<script setup>
import selectedRight from './selectedComponents/selectedRight.vue';
import { defineProps, defineEmits } from 'vue';
import draggable from 'vuedraggable';

defineProps({
  dataRight: Array,
  choosedItem: String,
});
defineEmits('chooseItem');
</script>
