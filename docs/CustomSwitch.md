# CustomSwitch

## Description

The `CustomSwitch` component is a toggle switch that can be used to switch between two states.

## Usage

```vue
<template>
  <CustomSwitch v-model="switchValue" />
</template>

<script>
import CustomSwitch from 'my-component-library/components/CustomSwitch.vue';

export default {
  components: {
    CustomSwitch,
  },
  data() {
    return {
      switchValue: false,
    };
  },
};
</script>