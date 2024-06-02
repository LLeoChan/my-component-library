# NavigationMenu

## Description

The `NavigationMenu` component provides a navigation menu.

## Usage

```vue
<template>
  <NavigationMenu :items="menuItems" />
</template>

<script>
import NavigationMenu from 'my-component-library/components/NavigationMenu.vue';

export default {
  components: {
    NavigationMenu,
  },
  data() {
    return {
      menuItems: [
        { name: 'Home', link: '/' },
        { name: 'About', link: '/about' },
        { name: 'Contact', link: '/contact' },
      ],
    };
  },
};
</script>