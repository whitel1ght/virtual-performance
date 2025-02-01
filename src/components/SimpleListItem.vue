<template>
  <div class="list-item">
    {{ item.name }}
  </div>
</template>

<script setup>
const props = defineProps({
  item: {
    type: Array,
    default: () => []
  }
})
</script>

<style lang="css">
.list-item {
  height: 100px;
  background-color: #fff;
  border-bottom: 1px solid #e0e0e0;
  padding: 20px;
}
</style>
