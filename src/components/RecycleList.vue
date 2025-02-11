<template>
  <RecycleScroller
    class="items-list"
    :items="items"
    :item-size="100"
    style="height: 600px;"
  >
    <template #default="{ item }">
      <list-item :item="item" />
    </template>
  </RecycleScroller>
</template>

<script setup>
import { RecycleScroller } from 'vue-virtual-scroller'
import ListItem from '@/components/ListItem.vue'
import 'vue-virtual-scroller/dist/vue-virtual-scroller.css'

const items = Array.from({ length: 1000 }, (_, i) => ({
  id: i,
  name: `Item ${i}`,
  description: `Description ${i}`
}))

</script>

<style>
.items-list {
  background-color: #f5f5f5;
  height: 600px;
  width: 600px;
  overflow-y: auto;
  margin: auto;
}
</style>
