<template>
  <div v-if="visible" :class="['message', type]">
    {{ message }}
  </div>
</template>

<script>
export default {
  name: 'GlobalMessage', // 修改组件名称为多词名称
  data() {
    return {
      visible: false,
      message: '',
      type: '',
    };
  },
  methods: {
    show(message, type = 'info') {
      this.message = message;
      this.type = type;
      this.visible = true;
      setTimeout(() => {
        this.visible = false;
      }, 3000);
    },
  },
};
</script>

<style scoped>
/* 样式保持不变 */
</style>
