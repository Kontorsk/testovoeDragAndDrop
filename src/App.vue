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

const dataLeft = ref([
  {
    id: 1,
    name: 'Shoes 1',
  },
  {
    id: 2,
    name: 'Shoes 2',
  },
  {
    id: 3,
    name: 'Shoes 3',
  },
  {
    id: 4,
    name: 'Shoes 4',
  },
  {
    id: 5,
    name: 'T-shirt 1',
  },
  {
    id: 6,
    name: 'T-shirt 2',
  },
  {
    id: 7,
    name: 'T-shirt 3',
  },
  {
    id: 8,
    name: 'T-shirt 4',
  },
]);
const dataRight = ref([
  {
    id: 11,
    name: 'Jacket 1',
  },
  {
    id: 12,
    name: 'Jacket 2',
  },
  {
    id: 13,
    name: 'Jacket 3',
  },
  {
    id: 14,
    name: 'Jacket 4',
  },
  {
    id: 15,
    name: 'Hoodie 1',
  },
  {
    id: 16,
    name: 'Hoodie 2',
  },
  {
    id: 17,
    name: 'Hoodie 3',
  },
  {
    id: 18,
    name: 'Hoodie 4',
  },
]);

const selectedArray = ref([]);
const choosedItem = ref('');

function selectItem(id) {
  dataLeft.value.forEach((element) => {
    if (
      element.id === id &&
      !selectedArray.value.includes(element) &&
      selectedArray.value.length < 6
    ) {
      selectedArray.value.push(element);
    }
  });
}

function chooseItem(id) {
  dataRight.value.forEach((element) => {
    if (element.id === id && !choosedItem.value.includes(element)) {
      choosedItem.value = element.name;
    }
  });
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
