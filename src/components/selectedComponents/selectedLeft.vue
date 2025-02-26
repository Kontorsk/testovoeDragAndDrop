<template>
  <div>
    <ul class="list">
      <li
        v-for="item in data"
        :key="item.name"
        class="list-item"
      >
        <h3>{{ item.name }}</h3>
      </li>
    </ul>
  </div>
</template>

<script setup>
defineProps({
  data: {
    type: Array,
    required: true,
  },
});
</script>
