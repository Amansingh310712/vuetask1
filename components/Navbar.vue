<template>
    <header class="header">
      <nav class="navbar">
        <div class="logo">
          <a href="#">
            <img src="https://themewagon.github.io/pinwheel/images/logo.svg" alt="Pinewheel logo" />
          </a>
        </div>
        <ul class="nav-links">
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
  
      <!-- Image at the top right corner -->
      <img
        src="https://themewagon.github.io/pinwheel/images/banner-shape.svg"
        alt="Top Right Decoration"
        class="top-right-image"
      />
    </header>
  </template>
  
  <script setup>
  </script>
  
  <style scoped>
  .header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 15px 20px;
    background-color:transparent;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
    position: relative; /* Ensure the image is positioned relative to the header */
  }
  
  .logo {
    font-size: 24px;
    font-weight: bold;
    color: #e16d6d;
  }
  
  .dropdown {
    position: relative;
  }
  
  .dropdown-menu {
    display: none;
    position: absolute;
    top: 100%;
    left: 0;
    background-color: white;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
    list-style: none;
    padding: 10px 0;
    margin: 0;
    z-index: 1000;
  }
  
  .dropdown-menu li {
    padding: 5px 20px;
  }
  
  .dropdown:hover .dropdown-menu {
    display: block;
  }
  
  .signup-btn {
    padding: 10px 20px;
    background-color: white;
    color: black;
    border: none;
    border-radius: 50px;
    cursor: pointer;
  }
  
  .nav-links {
    display: flex;
    list-style: none;
    gap: 3rem;
    text-decoration: none;
    margin-left: 70px;
    color: black;
  }
  
  .nav-links .link {
    text-decoration: none;
    color: black;
  }
  
  .link:hover {
    color: orange;
  }
  
  .navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  
  /* Top Right Image */
  .top-right-image {
    position: absolute;
    top: -50px;
    right: -50px; 
    width: 400px;
    z-index: -1;
  }
  </style>
  