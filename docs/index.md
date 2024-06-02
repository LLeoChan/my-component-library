# My Component Library

这是我的组件库文档。

## 安装

```bash
npm i my-component-library_leochan532

# ConfigProvider

## Description

The `ConfigProvider` component provides global configuration for your application, such as theme and localization.

## Usage

```vue
<template>
  <ConfigProvider themeColor="#f0f0f0">
    <YourComponent />
  </ConfigProvider>
</template>

<script>
import ConfigProvider from 'my-component-library/components/ConfigProvider.vue';

export default {
  components: {
    ConfigProvider,
  },
};
</script>

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

# FormComponent

## Description

The `FormComponent` is a customizable form with validation rules.

## Usage

```vue
<template>
  <FormComponent />
</template>

<script>
import FormComponent from 'my-component-library/components/FormComponent.vue';

export default {
  components: {
    FormComponent,
  },
};
</script>

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

# ImageCarousel

## Description

The `ImageCarousel` component displays a carousel of images.

## Usage

```vue
<template>
  <ImageCarousel :images="imageList" />
</template>

<script>
import ImageCarousel from 'my-component-library/components/ImageCarousel.vue';

export default {
  components: {
    ImageCarousel,
  },
  data() {
    return {
      imageList: [
        'image1.jpg',
        'image2.jpg',
        'image3.jpg',
      ],
    };
  },
};
</script>
Props
