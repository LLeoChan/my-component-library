/* eslint-disable vue/multi-word-component-names */
<template>
  <div :class="['switch', { 'switch-on': value }]" @click="toggle">
    <div class="switch-handle"></div>
  </div>
</template>

<script>
export default {
  name: 'CustomSwitch',
  props: {
    value: {
      type: Boolean,
      default: false,
    },
  },
  methods: {
    toggle() {
      this.$emit('input', !this.value);
    },
  },
};
</script>

<style scoped>
.switch {
  width: 50px;
  height: 25px;
  background-color: #ccc;
  border-radius: 25px;
  position: relative;
  cursor: pointer;
}
.switch-on {
  background-color: var(--primary-color);
}
.switch-handle {
  width: 23px;
  height: 23px;
  background-color: white;
  border-radius: 50%;
  position: absolute;
  top: 1px;
  left: 1px;
  transition: left 0.3s;
}
.switch-on .switch-handle {
  left: 25px;
}
</style>
