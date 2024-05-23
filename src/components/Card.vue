<template>
  <div class="card">
    <div class="image-container">
      <img :src="url" alt="Clothing item image" class="card-image" />
    </div>
    <div class="card-content">
      <h2 class="item-title">{{ title }}</h2>
      <p class="item-description">{{ description }}</p>
      <button class="buy-button">Buy Now</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: {
    title: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      required: true,
    },
    url: {
      type: String,
      required: true,
    },
  },
};
</script>

<style>
.card {
  border: 1px solid #ddd;
  border-radius: 8px;
  overflow: hidden;
  width: 300px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
}

.image-container {
  width: 100%;
  height: 200px;
  overflow: hidden;
}

.card-image {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.card-content {
  padding: 16px;
}

.item-title {
  font-family: "Arial", sans-serif;
  font-size: 24px;
  color: #333; /* Warna biru tua */
}

.item-description {
  font-family: "Arial", sans-serif;
  font-size: 18px;
  color: #555; /* Warna abu-abu tua */
}

.buy-button {
  display: block;
  width: 100%;
  padding: 8px 16px;
  margin-top: 8px;
  font-family: "Arial", sans-serif;
  font-size: 16px;
  color: #fff;
  background-color: #6ab0de; /* Warna biru langit */
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

.buy-button:hover {
  background-color: #2c3e50; /* Warna biru tua lebih gelap saat dihover */
}
</style>
