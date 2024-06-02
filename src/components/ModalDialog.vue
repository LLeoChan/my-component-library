<template>
  <div v-if="visible" class="modal-overlay">
    <div class="modal">
      <div class="modal-header">
        <slot name="header"></slot>
        <button @click="close">Close</button>
      </div>
      <div class="modal-body">
        <slot name="body"></slot>
      </div>
      <div class="modal-footer">
        <slot name="footer"></slot>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ModalDialog', 
  props: {
    visible: {
      type: Boolean,
      default: false,
    },
  },
  methods: {
    close() {
      this.$emit('close');
    },
  },
};
</script>

<style>
.modal-overlay {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: rgba(0, 0, 0, 0.5);
  display: flex;
  align-items: center;
  justify-content: center;
}
.modal {
  background: #fff;
  padding: 20px;
  border-radius: 5px;
  width: 500px;
  max-width: 100%;
}
</style>
