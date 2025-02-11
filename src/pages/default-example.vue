<template>
  <MainLayout>
    <h1 class="text-center"> Default Virtual List Example for Any Framework</h1>

    <v-virtual-scroll
      :items="items"
      :height="600"
    >
      <template #default="{ item }">
        {{ item.name }}
      </template>
    </v-virtual-scroll>
  </MainLayout>
</template>

<script setup>
import MainLayout from '@/components/layouts/MainLayout.vue'

const items = Array.from({ length: 1000 }, (_, i) => ({
  id: i,
  name: `Item ${i}`
}))
</script>
