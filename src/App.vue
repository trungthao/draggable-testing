
<template>
  <div class="row container">
    <!-- <div class="column">
      <card-item v-for="item in data" :key="content" :content="item.content"></card-item>
    </div> -->

    <div class="column">
      <draggable v-model="data" group="people" @start="drag = true" @end="drag = false" item-key="content">
        <template #item="{ element }">
          <card-item :content="element.content"></card-item>
        </template>
      </draggable>
    </div>

    <div class="column">
      <draggable v-model="data" group="people" @start="drag = true" @end="drag = false" item-key="content">
        <template #item="{ element }">
          <card-item :content="element.content"></card-item>
        </template>
      </draggable>
    </div>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Beatae ducimus a explicabo tenetur distinctio eum odit et
      nobis. Cumque facilis, corporis excepturi odit praesentium saepe et autem recusandae veritatis quibusdam?</p>
    <!-- <div class="column">
      <card-item v-for="item in data" :key="content" :content="item.content"></card-item>
    </div> -->
  </div>
</template>

<script setup>
import { ref } from 'vue';
import { RouterLink, RouterView } from 'vue-router'
import CardItem from './components/CardItem.vue'
import draggable from 'vuedraggable'
const drag = ref(false);
const data = ref([{ content: 'Item 1', },
{ content: 'Item 2', },
{ content: 'Item 3', },
{ content: 'Item 4', },
{ content: 'Item 5', },
{ content: 'Item 6', },
{ content: 'Item 7', },
{ content: 'Item 8', },
{ content: 'Item 9', },
{ content: 'Item 10  ', }])

</script>

<style scoped>
.container {
  height: 100vh;
  background-color: gray;
}

.row {
  display: flex;
  flex-direction: row;
  gap: 20px;
}

.column {
  display: flex;
  flex-direction: column;
  width: 100px;
  justify-content: center;
  align-items: center;
  background-color: gray;
}
</style>
