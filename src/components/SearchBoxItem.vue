<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  props: ['label'],
  setup(props) {
    return { ...props }
  },
})
</script>

<template>
  <div class="flex-container align-center search-item">
    <div class="search-item_label">
      <slot name="label">{{ label }}</slot>
    </div>
    <div class="search-item_container">
      <slot></slot>
    </div>
  </div>
</template>

<style scoped>
.search-item + .search-item {
  margin-left: 16px;
}
.search-item_label {
  color: #555;
  line-height: 22px;
  font-size: 14px;
}
</style>
