# GlobalMessage

## Description

The `GlobalMessage` component is used to show global messages to the user.

## Usage

```vue
<template>
  <GlobalMessage ref="message" />
</template>

<script>
import GlobalMessage from 'my-component-library/components/GlobalMessage.vue';

export default {
  components: {
    GlobalMessage,
  },
  methods: {
    showMessage() {
      this.$refs.message.showMessage('Hello, world!');
    },
  },
};
</script>