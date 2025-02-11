<template>
  <MainLayout>
    <slide-layout>
      <div class="slide">
        <h1 class="text-center">Lists. Things to keep in mind.</h1>

        <ol>
          <li><strong>Usual List:</strong> 📄 A list that renders all items, suitable for small datasets.</li>
          <li><strong>Virtual List:</strong> 🖥️ A list that renders only the visible items, improving performance and memory efficiency.</li>
        </ol>
      </div>
    </slide-layout>
  </MainLayout>
</template>

<script setup>
import SlideLayout from '@/components/layouts/SlideLayout.vue'
import MainLayout from '@/components/layouts/MainLayout.vue'
</script>

