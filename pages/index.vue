<template>
    <div>
      <Navbar/>
      <section class="hero">
        <div class="content">
          <h1>Scale design & dev operations with Avocode Enterprise</h1>
          <p>
            A fully integrated suite of authentication & authorization products,
            Stytch’s platform removes the headache of.
          </p>
          <button class="theme-btn">Download The Theme</button>
        </div>
        <div class="chart">
          <img src="https://themewagon.github.io/pinwheel/images/banner-img.png" alt="Chart Image" />
          
        </div>
        
      </section>
      <Highlightingpart/>
    </div>
  </template>
  
  <script setup>
  import Navbar from '~/components/Navbar.vue';
  import Highlightingpart from '~/components/Highlightingpart.vue';
  </script>
  
  <style>
  
  body {
    font-family: "Arial", sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f9f9f9;
  }
  
  /* Hero Section Styles */
  .hero {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 50px 20px;
    color: white;
  }
  
  .content {
    max-width: 50%;
  }
  
  h1 {
    font-size: 55px;
    margin-bottom: 20px;
    color:black;
  }
  
  p {
    font-size: 16px;
    margin-bottom: 20px;
    color:grey;

  }
  
  .theme-btn {
    padding: 10px 20px;
    background-color: white;
    color: #020202;
    border: none;
    border-radius: 50px;
    cursor: pointer;
    height: 50px;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
  }
  
  .chart img {
    max-width: 500px;
    border-radius: 10px;
   
  }
  </style>
  