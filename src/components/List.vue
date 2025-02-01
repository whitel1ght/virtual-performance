<template>
  <virtual-list
    class="items-list"
    :items="items"
    :item-height="100"
  >
    <template #default="{ item }">
      <list-item :item="item" />
    </template>
  </virtual-list>
</template>

<script setup>
import { ref } from 'vue'
import ListItem from '@/components/ListItem.vue'

const items = ref([
  { id: 1, name: 'Item 1', description: 'Description 1'},
  { id: 2, name: 'Item 2', description: 'Description: 2' },
  { id: 3, name: 'Item 3', description: 'Description: 3' },
  { id: 4, name: 'Item 4', description: 'Description: 4' },
  { id: 5, name: 'Item 5', description: 'Description: 5' },
  { id: 6, name: 'Item 6', description: 'Description: 6' },
  { id: 7, name: 'Item 7', description: 'Description: 7' },
  { id: 8, name: 'Item 8', description: 'Description: 8' },
  { id: 9, name: 'Item 9', description: 'Description: 9' },
  { id: 10, name: 'Item 10', description: 'Description: 10' },
  { id: 11, name: 'Item 11', description: 'Description: 11' },
  { id: 12, name: 'Item 12', description: 'Description: 12' },
  { id: 13, name: 'Item 13', description: 'Description: 13' },
  { id: 14, name: 'Item 14', description: 'Description: 14' },
  { id: 15, name: 'Item 15', description: 'Description: 15' },
  { id: 16, name: 'Item 16', description: 'Description: 16' },
  { id: 17, name: 'Item 17', description: 'Description: 17' },
  { id: 18, name: 'Item 18', description: 'Description: 18' },
  { id: 19, name: 'Item 19', description: 'Description: 19' },
  { id: 20, name: 'Item 20', description: 'Description: 20' },
  { id: 21, name: 'Item 21', description: 'Description: 21' },
  { id: 22, name: 'Item 22', description: 'Description: 22' },
  { id: 23, name: 'Item 23', description: 'Description: 23' },
  { id: 24, name: 'Item 24', description: 'Description: 24' },
  { id: 25, name: 'Item 25', description: 'Description: 25' },
  { id: 26, name: 'Item 26', description: 'Description: 26' },
  { id: 27, name: 'Item 27', description: 'Description: 27' },
  { id: 28, name: 'Item 28', description: 'Description: 28' },
  { id: 29, name: 'Item 29', description: 'Description: 29' },
  { id: 30, name: 'Item 30', description: 'Description: 30' },
  { id: 31, name: 'Item 31', description: 'Description: 31' },
  { id: 32, name: 'Item 32', description: 'Description: 32' },
  { id: 33, name: 'Item 33', description: 'Description: 33' },
  { id: 34, name: 'Item 34', description: 'Description: 34' }
])
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
