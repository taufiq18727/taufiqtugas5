<template>
  <div id="app">
    <Navbar />
    <div class="container mt-4">
      <Carousel />
      <div class="card-container mt-4">
        <Card 
          v-for="product in products" 
          :key="product.id" 
          :title="product.name" 
          :description="product.description" 
          :url="product.url" 
        />
      </div>
    </div>
    <Footer />
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue';
import Carousel from './components/Carousel.vue';
import Card from './components/Card.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    Navbar,
    Carousel,
    Card,
    Footer
  },
  data() {
    return {
      products: [
        { 
          id: 1, 
          name: 'Winter Clothes', 
          description: 'Warm your body in winter', 
          url: 'https://i5.walmartimages.com/asr/8c6eee8b-d4af-457d-9842-9789dbc4ffc0.26351d4005fdeeff86253468f5657af4.jpeg?odnHeight=2000&odnWidth=2000&odnBg=FFFFFF' 
        },
        { 
          id: 2, 
          name: 'snow glove', 
          description: 'glove for keep your hand safe from snow.', 
          url: 'https://images.tokopedia.net/img/cache/500-square/VqbcmM/2023/11/22/5057daf9-4128-4bba-92c5-7b8b44a370d1.jpg' 
        },
        { 
          id: 3, 
          name: 'Knit Hat', 
          description: 'cool knit hat for snow.', 
          url: 'https://png.pngtree.com/thumb_back/fw800/background/20230903/pngtree-one-of-the-hats-in-the-snow-that-has-flowers-on-image_13201520.jpg' 
        },
        { 
          id: 4, 
          name: 'Kids\' Jacket', 
          description: 'Warm and cozy jacket for kids.', 
          url: 'https://image.uniqlo.com/UQ/ST3/AsianCommon/imagesgoods/460160/sub/goods_460160_sub15.jpg?width=494' 
        },
        { 
          id: 5, 
          name: 'Scarf', 
          description: 'Comfortable and smorth make yourself comfortable in winter', 
          url: 'https://s.widget-club.com/images/YyiR86zpwIMIfrCZoSs4ulVD9RF3/b50ee9c2bf5276cdd13b994ed38ddc81/e2c7fb1f47146d69e89bd0f245ea5bec.jpg?q=70&w=500' 
        },
        { 
          id: 6, 
          name: 'Winter Boots', 
          description: 'walk on snow with Your new boots', 
          url: 'https://www.switchbacktravel.com/sites/default/files/articles%20/Winter%20Boots%20%28Sorel%20Caribou%20in%20snow%20-%20m%29.jpg' 
        }
      ]
    };
  }
};
</script>

<style>
body {
  background-color: #ecf0f1; /* Warna abu-abu */
}

.container {
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;
  padding: 16px;
}

.card-container {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 16px;
}
</style>
