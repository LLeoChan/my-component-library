<template>
  <div :class="`theme-${theme}`">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: 'ConfigProvider',
  props: {
    theme: {
      type: String,
      default: 'light',
    },
    locale: {
      type: Object,
      default: () => ({}),
    },
  },
  provide() {
    return {
      locale: this.locale,
    };
  },
};
</script>

<style scoped>
.theme-light {
  --primary-color: #1890ff;
}
.theme-dark {
  --primary-color: #001529;
}
</style>
