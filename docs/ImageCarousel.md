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