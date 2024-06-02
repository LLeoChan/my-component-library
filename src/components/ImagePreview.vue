<template>
  <div>
    <img :src="src" @click="showPreview = true" />
    <div v-if="showPreview" class="image-preview-overlay" @click="showPreview = false">
      <div class="image-preview" @click.stop>
        <img :src="src" :style="styleObject" />
        <button @click="rotate">Rotate</button>
        <button @click="zoomIn">Zoom In</button>
        <button @click="zoomOut">Zoom Out</button>
        <button @click="showPreview = false">Close</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    src: {
      type: String,
      required: true,
    },
  },
  data() {
    return {
      showPreview: false,
      rotation: 0,
      scale: 1,
    };
  },
  computed: {
    styleObject() {
      return {
        transform: `rotate(${this.rotation}deg) scale(${this.scale})`,
      };
    },
  },
  methods: {
    rotate() {
      this.rotation += 90;
    },
    zoomIn() {
      this.scale += 0.1;
    },
    zoomOut() {
      this.scale -= 0.1;
    },
  },
};
</script>

<style>
.image-preview-overlay {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: rgba(0, 0, 0, 0.7);
  display: flex;
  align-items: center;
  justify-content: center;
}
.image-preview {
  background: #fff;
  padding: 20px;
  border-radius: 5px;
  text-align: center;
}
</style>
