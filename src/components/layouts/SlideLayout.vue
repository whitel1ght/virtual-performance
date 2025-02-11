<template>
  <div class="slide-wrapper">
    <slot name="default"></slot>
  </div>
</template>

<style lang="scss">
.slide-wrapper {
  width: 100%;
  height: calc(100vh - 56px);
  align-content: center;

  .slide {
    vertical-align: middle;
    background-color: #f5f5f5;
    padding: 40px;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    max-width: 800px;
    margin: 0 auto;
  }

  h1 {
    margin-top: 20px;
    font-size: 2.5em;
    color: #333;
  }

  ol {
    margin-top: 20px;
    font-size: 1.4em;
    color: #555;
  }

  li {
    margin-bottom: 10px;
  }

  strong {
    color: #000;
  }
}
</style>
