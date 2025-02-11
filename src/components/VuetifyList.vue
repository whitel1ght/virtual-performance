<template>
  <v-virtual-scroll
    class="items-list"
    :items="items"
    :height="600"
    :item-height="100"
  >
    <template #default="{ item }">
      <list-item :item="item" />
    </template>
  </v-virtual-scroll>
</template>

<script setup>
import ListItem from '@/components/ListItem.vue'

const items = Array.from({ length: 100 }, (_, i) => ({
  id: i,
  name: `Item ${i}`,
  description: `Description: ${i}`
}))
</script>

<style lang="scss">
.items-list {
  background-color: #f5f5f5;
  height: 600px;
  width: 600px;
  overflow-y: auto;
  margin: auto;
}
</style>
