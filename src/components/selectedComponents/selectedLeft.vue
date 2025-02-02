<template>
  <div>
    <ul class="list">
        <li class="list-item" v-for="item in data.slice(0, 6)" :key="item.id">
          <h3>{{ item.name }}</h3>
        </li>
      </ul>
  </div>
</template>

<script>
import {ref} from 'vue'

export default {
  setup() {
    const data = ref([])

    return {
      data,
    }
  },
};
</script>

