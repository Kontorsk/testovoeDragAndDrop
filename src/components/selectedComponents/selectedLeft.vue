<template>
  <div>
    <ul class="list">
        <li class="list-selected" v-for="item in data" :key="item.id">
          <div v-if="item.visible" class="list-item">
            <h3>{{ item.name }}</h3>
          </div>
        </li>
      </ul>
  </div>
</template>

<script>
export default {
  props: ["data"],
};
</script>

<style scoped>
.list-selected {
  display: inline-block;
  }
</style>
