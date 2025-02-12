<template>
  <div class="list-item">
    <div class="list-item__checkbox">
      <v-checkbox-btn density="compact" />
    </div>

    <div class="list-item__content">
      <div>{{ item.name }}</div>
      <div>{{ item.description }}</div>

      <div class="list-item__content-actions">
        <v-tooltip
          location="top"
          v-for="action in actions"
          :open-delay="300"
          :key="action.id"
        >
          <template #activator="{ props }">
            <v-btn
              density="compact"
              variant="text"
              :key="action.id"
              :icon="action.icon"
              @click="() => $emit(action.event, item)"
              v-bind="props"
              class="list-item__content-actions__btn"
            />
          </template>
          <span>{{ action.name }}</span>
        </v-tooltip>
      </div>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  item: {
    type: Object,
    default: () => []
  }
})

const actions = [
  {
    id: 1,
    event: 'refresh',
    name: 'Refresh',
    icon: 'mdi-refresh'
  },
  {
    id: 2,
    event: 'edit',
    name: 'Edit',
    icon: 'mdi-pencil'
  },
  {
    id: 3,
    event: 'delete',
    name: 'Delete',
    icon: 'mdi-delete'
  },
  {
    id: 4,
    event: 'copy',
    name: 'Copy',
    icon: 'mdi-content-copy'
  }
]
</script>

<style lang="scss">
.list-item {
  display: flex;
  height: 100px;
  background-color: #fff;
  border-bottom: 1px solid #e0e0e0;

  &__checkbox {
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 0 10px;
  }

  &__content {
    padding: 10px;
    display: flex;
    flex-grow: 1;
    flex-direction: column;
    justify-content: space-between;

    &-actions {
      display: flex;
      justify-content: flex-end;
      gap: 5px;
      width: 100%;
      height: 30px;

      .v-btn {
        display: none;
      }
    }
  }
}

.list-item:hover {
  background-color: #f5f5f5;

  .list-item__content-actions .v-btn {
    display: block;
  }
}
</style>
