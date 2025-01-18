<template>
  <div
    ref="containerRef"
    class="virtual-list"
  >
    <ul ref="ulRef">
      <li
        v-for="(item, index) in visibleData"
        :key="item[props.itemKeyField]"
        :data-id="item[props.itemKeyField]"
        :style="{
          top: `${(start + index) * props.itemHeight}px`,
          height: `${props.itemHeight}px`
        }"
        class="virtual-list__item"
      >
        <slot v-bind="{ item }" />
      </li>

      <li
        :style="placeholderStyle"
        class="placeholder"
      />
    </ul>
  </div>
</template>

<script setup>
import { ref, computed, onBeforeUnmount, onMounted } from 'vue'

const props = defineProps({
  items: {
    type: Array,
    default: () => []
  },
  selected: {
    type: Object,
    default: () => ({})
  },
  itemKeyField: {
    type: String,
    default: 'id'
  },
  buffer: {
    type: Number,
    default: 5
  },
  itemHeight: {
    type: Number,
    required: true
  },
  eventBus: Object
})

const emit = defineEmits(['select-item', 'toggle-item'])

const containerRef = ref(null)
const ulRef = ref(null)
const start = ref(0)

const fitsIntoScroll = computed(() => {
  return Math.floor(containerRef.value?.getBoundingClientRect().height / props.itemHeight) ?? 10
})

const end = computed(() => start.value + fitsIntoScroll.value + props.buffer)

const placeholderStyle = computed(() => ({
  height: `${props.items.length * props.itemHeight}px`
}))

const visibleData = computed(() => {
  return props.items
    .slice(start.value, Math.min(end.value, props.items.length))
})

const onScroll = () => {
  requestAnimationFrame(() => {
    const scrollTop = containerRef.value.scrollTop
    start.value = Math.floor(scrollTop / props.itemHeight)
  })
}

onMounted(() => {
  containerRef.value.addEventListener('scroll', onScroll)
})

onBeforeUnmount(() => {
  containerRef.value?.removeEventListener('scroll', onScroll)
})
</script>

<style lang="scss">
.virtual-list {
  display: flex;
  flex-direction: column;
  position: relative;
  overflow-y: auto;

  &__item {
    width: 100%;
    position: absolute;
    list-style: none;

    &::after {
      // content: '';
      // position: absolute;
      // inset: 0;
      // z-index: 5;
      // border-radius: $border-radius-base;
      // border: 3px solid var(--focus-color);
      // opacity: 0;
      // transition: opacity $transition-bezier;
      // pointer-events: none;
      // user-select: none;
    }
  }
}
</style>
