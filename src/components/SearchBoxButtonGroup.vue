<script lang="ts">
import { defineComponent, reactive } from 'vue'

export default defineComponent({
  setup() {
    const buttonList = reactive([
      { label: '查询', eventName: 'search', type: 'primary' },
      { label: '重置', eventName: 'reset' },
    ])
    return { buttonList };
  },
})
</script>

<template>
  <div>
    <button
      class="search-box_button"
      v-for="(button, idx) in buttonList"
      :key="idx"
      :class="button.type ? ('button_' + button.type) : ''"
    >{{ button.label }}</button>
  </div>
</template>

<style scoped>
.search-box_button {
  border-radius: 0;
}
.search-box_button + .search-box_button {
  margin-left: 16px;
}
.button_primary {
  background-color: #5677D6;
  color: #FFF;
}
</style>
