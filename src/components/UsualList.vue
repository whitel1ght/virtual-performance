<template>
  <ul class="usual-list">
    <li
      v-for="item in items"
      :key="item.id"
      class="usual-list__item"
    >
      <list-item :item="item" />
    </li>
  </ul>
</template>

<script setup>
import ListItem from '@/components/ListItem.vue'

const items = Array.from({ length: 100 }, (_, i) => ({
  id: i,
  name: `Item ${i}`,
  description: `Description for item ${i}`
}))
</script>

<style lang="scss">
.usual-list {
  height: 600px;
  overflow-y: auto;
}
</style>
