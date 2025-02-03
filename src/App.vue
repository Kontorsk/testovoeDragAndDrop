<template>
  <main>
    <TheLeftSpace
    :dataLeft="dataLeft"
    @changeVision="changeVision"
    />
    <TheRightSpace
    :dataRight="dataRight" />
  </main>
</template>

<script>
import {ref} from 'vue'
import TheLeftSpace from "./components/TheLeftSpace.vue";
import TheRightSpace from "./components/TheRightSpace.vue";

export default {
  components: {
    TheLeftSpace,
    TheRightSpace,
  },
  setup () {
    const dataLeft = ref([
    {
        "id": 1,
        "name": "Shoes 1",
        "visible": false
    },
    {
        "id": 2,
        "name": "Shoes 2",
        "visible": false
    },
    {
        "id": 3,
        "name": "Shoes 3",
        "visible": false
    },
    {
        "id": 4,
        "name": "Shoes 4",
        "visible": false
    },
    {
        "id": 5,
        "name": "T-shirt 1",
        "visible": false
    },
    {
        "id": 6,
        "name": "T-shirt 2",
        "visible": false
    },
    {
        "id": 7,
        "name": "T-shirt 3",
        "visible": false
    },
    {
        "id": 8,
        "name": "T-shirt 4",
        "visible": false
    }
    ])
    const dataRight = ref([
    {
        "id": 11,
        "name": "Jacket 1",
        "visible": false
    },
    {
        "id": 12,
        "name": "Jacket 2",
        "visible": false
    },
    {
        "id": 13,
        "name": "Jacket 3",
        "visible": false
    },
    {
        "id": 14,
        "name": "Jacket 4",
        "visible": false
    },
    {
        "id": 15,
        "name": "Hoodie 1",
        "visible": false
    },
    {
        "id": 16,
        "name": "Hoodie 2",
        "visible": false
    },
    {
        "id": 17,
        "name": "Hoodie 3",
        "visible": false
    },
    {
        "id": 18,
        "name": "Hoodie 4",
        "visible": false
    }
    ])

    let num = 0
    const counter = []

    function changeVision (id) {
      // console.log(dataLeft.value[id-1])
      // console.log(dataLeft.value[0].id)
      console.log(num)
      if (num <6) {
      dataLeft.value.forEach(element => {
        if (element.id===id && !counter.includes(id)) {
          element.visible=true
          num++
          counter.push(element.id)
        }
      })
      }
    }

    // const selected = []

    // function changeVision (id) {
    //   // console.log(dataLeft.value[id-1])
    //   // console.log(dataLeft.value[0].id)
    //   dataLeft.value.forEach(element => {
    //     if (element.id===id) {
    //       selected.push(element)
    //     }
    //   })
    // }

    return {
      dataLeft,
      dataRight,
      changeVision
    }
  }
};
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
