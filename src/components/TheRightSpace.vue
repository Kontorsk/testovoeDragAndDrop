<template>
  <div>
    <selectedRight class="selected" />
    <div class="components">
      <ul class="list">
        <li class="list-item" v-for="item in dataRight" :key="item.id">
          <h3>{{ item.name }}</h3>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
import selectedRight from './selectedComponents/selectedRight.vue';

export default {
  components: {selectedRight},
  props: ["dataRight"],
  setup() {
    return {};
  },
};
</script>
