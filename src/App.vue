<template>
  <main>
    <TheLeftSpace
      :dataLeft="dataLeft"
      :selectedArray="selectedArray"
      @selectItem="selectItem"
    />
    <TheRightSpace
      :dataRight="dataRight"
      :choosedItem="choosedItem"
      @chooseItem="chooseItem"
    />
  </main>
</template>

<script setup>
import { ref } from 'vue';
import TheLeftSpace from './components/TheLeftSpace.vue';
import TheRightSpace from './components/TheRightSpace.vue';

const dataLeft = ref(createData('Shoes'));
const dataRight = ref(createData('Jacket'));

const selectedArray = ref([]);
const choosedItem = ref('');

function createData(title) {
  return Array.from({ length: 10 }, (_, i) => ({ name: `${title} ${++i}` }));
}

function selectItem(name) {
  if (selectedArray.value.length >= 6 || selectedArray.value.includes(name)) {
    return;
  }
  dataLeft.value.forEach((element) => {
    if (element.name === name) {
      selectedArray.value.push(element);
    }
  });
}

function chooseItem(name) {
  const item = dataRight.value.find((elem) => {
    return elem.name === name;
  });
  choosedItem.value = item.name;
}
</script>

<style>
main {
  margin: 2.5% 15%;
  display: flex;
  justify-content: space-between;
  width: auto;
}

.components {
  border: 3px solid;
  width: 600px;
  height: 800px;
}

.selected {
  border: 3px solid;
  width: 350px;
  height: 265px;
  margin-bottom: 50px;
}

.list {
  margin: 10px 10px 0 10px;
  padding: 0;
  list-style: none;
}

.list-item {
  display: inline-block;
  border: 2px dashed;
  margin: 10px;
  width: 80px;
  text-align: center;
}
</style>
