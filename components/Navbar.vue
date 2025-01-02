<template>
  <header class="header">
    <nav class="navbar">
      <div class="logo">
        <a href="#">
          <img src="https://themewagon.github.io/pinwheel/images/logo.svg" alt="Pinewheel logo" />
        </a>
      </div>

      <!-- Hamburger Menu -->
      <div class="hamburger" @click="toggleMenu">
        <div class="line"></div>
        <div class="line"></div>
        <div class="line"></div>
      </div>

      <!-- Navigation Links -->
      <ul :class="['nav-links', isMenuOpen ? 'show' : '']">
        <li><a href="#" class="link">Home</a></li>
        <li><a href="#" class="link">About</a></li>
        <li><a href="#" class="link">Blog</a></li>
        <li><a href="#" class="link">Features</a></li>
        <li><a href="#" class="link">How It Works</a></li>
        <li class="dropdown">
          <a href="#" class="link">Pages</a>
          <ul class="dropdown-menu">
            <li><a href="#" class="link">Career</a></li>
            <li><a href="#" class="link">Career Single</a></li>
            <li><a href="#" class="link">Integrations</a></li>
            <li><a href="#" class="link">Integration Single</a></li>
            <li><a href="#" class="link">Pricing</a></li>
            <li><a href="#" class="link">Changelogs</a></li>
            <li><a href="#" class="link">Terms and Conditions</a></li>
          </ul>
        </li>
        <li><a href="#" class="link">Contact</a></li>
      </ul>
    </nav>

    <button class="signup-btn">Sign Up Now</button>

    
  </header>
</template>

<script setup>
import { ref } from 'vue';

const isMenuOpen = ref(false);

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value;
};
</script>

<style scoped>
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 15px 20px;
  background-color: transparent;
  position: relative;
}

.logo {
  font-size: 24px;
  font-weight: bold;
  color: #e16d6d;
}

.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
}

.nav-links {
  display: flex;
  list-style: none;
  gap: 3rem;
  text-decoration: none;
  /* margin-left: 70px; */
  color: black;
}

.nav-links .link {
  text-decoration: none;
  color: black;
}

.link:hover {
  color: orange;
}

.signup-btn {
  padding: 10px 20px;
  background-color: white;
  color: black;
  border: none;
  border-radius: 50px;
  cursor: pointer;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
}

/* Hamburger Menu */
.hamburger {
  display: none;
  flex-direction: column;
  gap: 5px;
  cursor: pointer;
}

.hamburger .line {
  width: 25px;
  height: 3px;
  background-color: black;
}

/* Dropdown */
.dropdown {
  position: relative;
}

.dropdown-menu {
  display: none;
  position: absolute;
  top: 100%;
  left: 0;
  background-color: white;
  list-style: none;
  padding: 10px 0;
  margin: 0;
  width: 200px;
  z-index: 1000;
}

.dropdown-menu li {
  padding: 5px 20px;
}

.dropdown:hover .dropdown-menu {
  display: block;
}

/* Top Right Image */


/* Responsive Styles */
@media (max-width: 768px) {
  .nav-links {
    display: none;
    flex-direction: column;
    position: absolute;
    top: 70px;
    right: 20px;
    background: white;
    width: 250px;
    border-radius: 8px;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
    padding: 20px;
    z-index: 1000;
  }

  .nav-links.show {
    display: flex;
  }

  .hamburger {
    display: flex;
  }

  .signup-btn {
    display: none;
  }
}
</style>
  