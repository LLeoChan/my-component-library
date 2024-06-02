# ModalDialog

## Description

The `ModalDialog` component is a modal dialog box.

## Usage

```vue
<template>
  <ModalDialog :visible="isVisible" @close="isVisible = false">
    <template #header>
      <h2>Modal Header</h2>
    </template>
    <template #body>
      <p>Modal body content goes here.</p>
    </template>
    <template #footer>
      <button @click="isVisible = false">Close</button>
    </template>
  </ModalDialog>
</template>

<script>
import ModalDialog from 'my-component-library/components/ModalDialog.vue';

export default {
  components: {
    ModalDialog,
  },
  data() {
    return {
      isVisible: false,
    };
  },
};
</script>