<template>
  <ConfigProvider :theme="theme">
    <CustomSwitch v-model="switchValue" @input="toggleSwitch" />
    <GlobalMessage ref="message" />
    <button @click="showMessage">Show Message</button>
    <InfiniteList :items="items" />
  </ConfigProvider>
</template>

<script>
import ConfigProvider from './components/ConfigProvider.vue';
import CustomSwitch from './components/CustomSwitch.vue';
import GlobalMessage from './components/GlobalMessage.vue'; // 修改引入的组件名
import InfiniteList from './components/InfiniteList.vue';

export default {
  name: 'App',
  components: {
    ConfigProvider,
    CustomSwitch,
    GlobalMessage,
    InfiniteList, // 修改组件名
  },
  data() {
    return {
      theme: 'light',
      switchValue: false,
    };
  },
  methods: {
    toggleSwitch(value) {
      this.switchValue = value;
      this.$refs.message.show(`Switch is now ${value ? 'On' : 'Off'}`, 'info');
    },
    showMessage() {
      this.$refs.message.show('This is a global message!', 'success');
    },
  },
};
</script>

<style>
/* 你的全局样式可以放在这里 */
</style>
