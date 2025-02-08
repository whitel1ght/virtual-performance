<template>
  <slide-layout>
    <div class="slide">
      <h1 class="text-center">Virtual List Pros:</h1>

      <ol>
        <li><strong>Performance:</strong> Virtual scrolling improves performance by rendering only the visible items in the list, reducing the load on the browser.</li>
        <li><strong>Memory Efficiency:</strong> It uses less memory since only a subset of the data is rendered at any given time.</li>
        <li><strong>Smooth Scrolling</strong>: Provides a smoother scrolling experience, especially with large datasets.</li>
        <li><strong>Faster Load Times</strong>: Initial load times are faster because the entire dataset does not need to be rendered.</li>
        <li><strong>Scalability</strong>: Can handle large datasets efficiently, making it suitable for applications with extensive data.</li>
      </ol>
    </div>
  </slide-layout>
</template>

<script setup>
import SlideLayout from '@/components/layouts/SlideLayout.vue'
</script>

