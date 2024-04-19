<script lang="ts">
import { defineComponent, ref, defineAsyncComponent } from "vue";

export default defineComponent({
  components: {
    SeachBoxBuutonGroup: defineAsyncComponent(() => import('./SearchBoxButtonGroup.vue'))
  },
  props: ['searchForm'],
  setup(props) {
    const isShow = ref(true);
    const searchForm = props.searchForm;
    return {
      isShow,
      searchForm,
    };
  },
});
</script>

<template>
  <div class="flex-container space-between">
    <div class="flex-container align-center">
      <slot></slot>
    </div>
    <SeachBoxBuutonGroup></SeachBoxBuutonGroup>
  </div>
</template>

<style scoped>

</style>
