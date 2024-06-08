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
import GlobalMessage from './components/GlobalMessage.vue'; 
import ImagePreview from './components/ImagePreview.vue';
import ImageCarousel from './component/ImageCarousel.vue';
import FormComponent from './component/FormComponent.vue';


export default {
  name: 'App',
  components: {
    ConfigProvider,
    CustomSwitch,
    GlobalMessage,
    ImagePreview,
    ImageCarousel,
    FormComponent,
    
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

</style>
