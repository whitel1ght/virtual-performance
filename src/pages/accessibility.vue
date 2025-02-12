<template>
  <MainLayout>
    <SlideLayout>
      <div class="slide">
        <h1>Making Virtual Scrolling Accessible</h1>

        <ol>
          <li><strong>ARIA Roles and Properties:</strong> Use appropriate ARIA roles and properties to convey structure and size.</li>
          <li><strong>Keyboard Navigation:</strong> Ensure seamless keyboard navigation with arrow keys.</li>
          <li><strong>Focus Management:</strong> Maintain focus on the selected item and manage focus dynamically.</li>
          <li><strong>Lazy Loading Announcements:</strong> Use live regions to announce new content loading.</li>
          <li><strong>Semantic HTML:</strong> Use semantic HTML elements where possible.</li>
          <li><strong>Consistent Layout:</strong> Ensure a consistent and predictable layout as new items load.</li>
          <li><strong>Testing with Assistive Technologies:</strong> Regularly test with screen readers and other assistive technologies.</li>
        </ol>
      </div>
    </SlideLayout>
  </MainLayout>
</template>

<script setup>
import SlideLayout from '@/components/layouts/SlideLayout.vue'
import MainLayout from '@/components/layouts/MainLayout.vue'
</script>
