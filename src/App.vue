<script setup>
import { reactive } from 'vue';
import SearchBox from './components/SearchBox.vue';
import SearchBoxItem from './components/SearchBoxItem.vue';
const searchForm = reactive({
  
});
</script>

<template>
  <SearchBox
    :search-form="searchForm"
  >
    <SearchBoxItem label="输入款：">
      <input type="text">
    </SearchBoxItem>
    <SearchBoxItem label="下拉框：">
      <select>
        <option>1</option>
        <option>2</option>
        <option>3</option>
      </select>
    </SearchBoxItem>
  </SearchBox>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
