<template>
  <nav class="navbar">
    <div class="logo">
      <img src="https://dynamic.brandcrowd.com/asset/logo/3908a892-8811-4bdb-ac0d-f4c740688a34/logo-search-grid-1x?logoTemplateVersion=1&v=637707471720030000&text=FrostWear" alt="Logo" class="logo-image" />
      <span class="logo-text">Frost Wear</span>
    </div>
    <div class="hamburger-menu" @click="toggleMenu">
      <div class="bar"></div>
      <div class="bar"></div>
      <div class="bar"></div>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'Navbar',
  data() {
    return {
      isMenuOpen: false
    };
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen;
    }
  }
}
</script>

<style>
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #6ab0de; /* Warna biru langit */
  padding: 10px;
  position: relative;
}

.logo {
  display: flex;
  align-items: center;
}

.logo-image {
  width: 40px;
  height: auto;
  margin-right: 10px;
}

.logo-text {
  color: #fff;
  font-size: 24px;
  font-family: 'Arial', sans-serif;
}

.hamburger-menu {
  display: none;
  flex-direction: column;
  cursor: pointer;
}

.bar {
  width: 25px;
  height: 3px;
  background-color: #fff;
  margin: 3px 0;
  transition: transform 0.3s, opacity 0.3s;
}

@media (max-width: 768px) {
  .hamburger-menu {
    display: flex;
  }
}
</style>
