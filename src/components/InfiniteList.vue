<template>
  <div class="infinite-list" ref="scrollContainer" @scroll="handleScroll">
    <div v-for="(item, index) in visibleItems" :key="index" class="list-item">
      {{ item }}
    </div>
  </div>
</template>

<script>
export default {
  name: 'InfiniteList',
  props: {
    items: {
      type: Array,
      required: true,
    },
  },
  data() {
    return {
      visibleItems: [],
      startIndex: 0,
      endIndex: 10, // 初始显示的列表项数
      itemsPerLoad: 10, // 每次加载的列表项数
    };
  },
  mounted() {
    this.updateVisibleItems();
  },
  methods: {
    handleScroll() {
      const container = this.$refs.scrollContainer;
      if (container.scrollTop + container.clientHeight >= container.scrollHeight) {
        this.loadMoreItems();
      }
    },
    updateVisibleItems() {
      this.visibleItems = this.items.slice(this.startIndex, this.endIndex);
    },
    loadMoreItems() {
      this.startIndex = this.endIndex;
      this.endIndex += this.itemsPerLoad;
      this.updateVisibleItems();
    },
  },
};
</script>

<style scoped>
.infinite-list {
  height: 300px; /* 设置列表容器的高度 */
  overflow-y: auto; /* 允许垂直滚动 */
}

.list-item {
  padding: 10px;
  border-bottom: 1px solid #ccc; /* 添加分隔线 */
}
</style>
