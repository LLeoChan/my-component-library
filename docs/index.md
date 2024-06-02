# My Component Library

这是我的组件库文档。

## 安装

bash
已上传npm
npm i my-component-library_leochan532

# ConfigProvider

## Description

“ConfigProvider”组件为您的应用程序提供全局配置，例如主题和本地化。

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

`CustomSwitch` 组件是一个切换开关，可用于在两种状态之间切换。

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

`FormComponent` 是一个带有验证规则的可定制表单。

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

`GlobalMessage` 组件用于向用户显示全局消息。

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

`ImageCarousel` 组件显示图像轮播。

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
