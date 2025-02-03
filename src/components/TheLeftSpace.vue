<template>
  <div>
    <selectedLeft :data="dataLeft" class="selected" />
    <div class="components">
      <ul class="list">
        <li @click="$emit('changeVision', item.id)" class="list-item" v-for="item in dataLeft" :key="item.id">
          <h3>{{ item.name }}</h3>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
import selectedLeft from './selectedComponents/selectedLeft.vue';

export default {
  components: {selectedLeft},
  props: ["dataLeft"],
  setup() {
    return {};
  },
};
</script>

