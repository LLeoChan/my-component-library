<template>
  <div class="carousel">
    <div class="carousel-inner" :style="{ transform: `translateX(-${currentIndex * 100}%)` }">
      <div v-for="(image, index) in images" :key="index" class="carousel-item">
        <img :src="image" alt="">
      </div>
    </div>
    <button @click="prev">Prev</button>
    <button @click="next">Next</button>
  </div>
</template>

<script>
export default {
  name: 'ImageCarousel',
  props: {
    images: {
      type: Array,
      required: true,
    },
  },
  data() {
    return {
      currentIndex: 0,
    };
  },
  methods: {
    prev() {
      this.currentIndex = (this.currentIndex - 1 + this.images.length) % this.images.length;
    },
    next() {
      this.currentIndex = (this.currentIndex + 1) % this.images.length;
    },
  },
};
</script>

<style>
.carousel {
  position: relative;
  overflow: hidden;
  width: 100%;
  height: 300px;
}
.carousel-inner {
  display: flex;
  transition: transform 0.5s ease;
}
.carousel-item {
  min-width: 100%;
}
button {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
}
button:nth-child(2) {
  left: 10px;
}
button:nth-child(3) {
  right: 10px;
}
</style>
