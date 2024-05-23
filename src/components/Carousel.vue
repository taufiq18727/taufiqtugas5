<template>
  <div class="carousel">
    <!-- Add carousel implementation here -->
    <img :src="images[currentImageIndex]" alt="Carousel image" class="carousel-image" />
    <button @click="prevImage" class="carousel-button prev">&#10094;</button>
    <button @click="nextImage" class="carousel-button next">&#10095;</button>
  </div>
</template>

<script>
export default {
  name: 'Carousel',
  data() {
    return {
      images: [
        'https://img.freepik.com/free-vector/flat-design-winter-sale-special-offer-promo_23-2148721764.jpg',
        'https://www.switchbacktravel.com/sites/default/files/articles%20/Winter%20Boots%20%28Sorel%20Caribou%20in%20snow%20-%20m%29.jpg',
        'https://static.vecteezy.com/system/resources/previews/003/609/335/non_2x/sticker-set-of-clothes-for-winter-celebration-free-vector.jpg'
      ],
      currentImageIndex: 0
    };
  },
  methods: {
    prevImage() {
      this.currentImageIndex = (this.currentImageIndex - 1 + this.images.length) % this.images.length;
    },
    nextImage() {
      this.currentImageIndex = (this.currentImageIndex + 1) % this.images.length;
    }
  }
};
</script>

<style>
.carousel {
  display: flex;
  align-items: center;
  justify-content: center;
  overflow: hidden;
  position: relative;
  background-color: #87ceeb; /* Warna biru muda */
  height: 400px;
}

.carousel-image {
  width: 100%;
  height: auto;
}

.carousel-button {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  background-color: rgba(255, 255, 255, 0.7);
  color: #333;
  border: none;
  padding: 10px;
  cursor: pointer;
  font-size: 24px;
  z-index: 2;
}

.carousel-button.prev {
  left: 10px;
}

.carousel-button.next {
  right: 10px;
}

.carousel-button:hover {
  background-color: rgba(255, 255, 255, 0.9);
}
</style>
