<template>
  <MainLayout>
    <SlideLayout>
      <div class="slide">
        <h1 class="text-center">Virtual List Cons:</h1>
          <ol>
            <li>🔍 <strong>Complexity:</strong> Implementing virtual scrolling can be more complex compared to traditional scrolling methods.</li>
            <li>🛠️ <strong>Maintenance:</strong> Requires additional maintenance and debugging effort, especially for edge cases.</li>
            <li>📊 <strong>Data Handling:</strong> May require special handling for certain types of data or interactions, such as infinite scrolling or dynamic content loading.</li>
           <li>📉 <strong>SEO Impact:</strong> Content that is not rendered initially may not be indexed by search engines, potentially impacting SEO.</li>
           <li>🖥️ <strong>Compatibility:</strong> May have compatibility issues with older browsers or devices with limited resources.</li>
           <li>♿ <strong>Accessibility:</strong> Virtual scrolling can create challenges for screen readers and keyboard navigation, potentially impacting accessibility.</li>
         </ol>
      </div>
    </SlideLayout>
  </MainLayout>
</template>

<script setup>
import SlideLayout from '@/components/layouts/SlideLayout.vue'
import MainLayout from '@/components/layouts/MainLayout.vue'
</script>
