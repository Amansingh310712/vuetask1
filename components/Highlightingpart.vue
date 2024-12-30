<template>
    <section class="highlighting-part">
      <div class="container">
        <div class="header">
          <div class="text-content">
            <h2>The Highlighting Part Of Our Solution</h2>
          </div>
          <div class="title">
            <p>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi egestas
              Werat viverra id et aliquet. Vulputate egestas sollicitudin.
            </p>
          </div>
        </div>
        <div class="cards">
          <div class="card" v-for="(feature, index) in features" :key="index">
            <div class="icon" :style="{ color: feature.iconColor }">
              <i :class="feature.iconClass"></i>
            </div>
            <h3>{{ feature.title }}</h3>
            <p>{{ feature.description }}</p>
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script setup>
  const features = [
    {
      title: "Live Caption",
      description: "Lorem ipsum dolor sit amet consectetur, adipiscing elit.",
      iconClass: "fas fa-tv", // Replace with your icon class
      iconColor: "#ff6b6b",
    },
    {
      title: "Smart Reply",
      description: "Lorem ipsum dolor sit amet consectetur, adipiscing elit.",
      iconClass: "fas fa-paperclip",
      iconColor: "#ff6b6b",
    },
    {
      title: "Sound Amplifier",
      description: "Lorem ipsum dolor sit amet consectetur, adipiscing elit.",
      iconClass: "fas fa-bell",
      iconColor: "#ff6b6b",
    },
    {
      title: "Gesture Navigation",
      description: "Lorem ipsum dolor sit amet consectetur, adipiscing elit.",
      iconClass: "fas fa-mouse-pointer",
      iconColor: "#ff6b6b",
    },
    {
      title: "Dark Theme",
      description: "Lorem ipsum dolor sit amet consectetur, adipiscing elit.",
      iconClass: "fas fa-lightbulb",
      iconColor: "#ff6b6b",
    },
    {
      title: "Privacy Controls",
      description: "Lorem ipsum dolor sit amet consectetur, adipiscing elit.",
      iconClass: "fas fa-lock",
      iconColor: "#ff6b6b",
    },
    {
      title: "Location Controls",
      description: "Lorem ipsum dolor sit amet consectetur, adipiscing elit.",
      iconClass: "fas fa-map-marker-alt",
      iconColor: "#ff6b6b",
    },
    {
      title: "Security Updates",
      description: "Lorem ipsum dolor sit amet consectetur, adipiscing elit.",
      iconClass: "fas fa-shield-alt",
      iconColor: "#ff6b6b",
    },
    {
      title: "Focus Mode",
      description: "Lorem ipsum dolor sit amet consectetur, adipiscing elit.",
      iconClass: "fas fa-shield-alt",
      iconColor: "#ff6b6b",
    },
    {
      title: "Family Link",
      description: "Lorem ipsum dolor sit amet consectetur, adipiscing elit.",
      iconClass: "fas fa-shield-alt",
      iconColor: "#ff6b6b",
    },
  ];
  </script>
  
  <style scoped>
  .highlighting-part {
    padding: 50px 20px;
    background-color: #f8f9fa;
  }
  
  .container {
    max-width: 1200px;
    margin: 0 auto;
  }
  
  .header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 30px;
    text-align: left;
  }
  
  .text-content {
    flex: 1;
    font-size: 1.5rem;
    color:black;
    margin-right: 20px;
  }
  
  .title {
    flex:1;
    text-align: right;
  }
  
  .title h2 {
    font-weight: 700;
    margin: 0;
  }
  
  .cards {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 20px;
  }
  
  .card {
    background: #fff;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
    text-align: left;
    transition: transform 0.2s ease;
  }
  
  .card:hover {
    transform: translateY(-5px);
  }
  
  .card .icon {
    font-size: 2rem;
    margin-bottom: 10px;
  }
  
  .card h3 {
    font-size: 1.2rem;
    margin-bottom: 10px;
    font-weight: 600;
  }
  
  .card p {
    font-size: 0.9rem;
    color: #6c757d;
  }
  </style>
  