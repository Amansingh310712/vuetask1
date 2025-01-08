<template>
    <div style="position: relative;">
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
        <!-- Image at the top right corner -->
        <img src="https://themewagon.github.io/pinwheel/images/banner-shape.svg" alt="Top Right Decoration"
            class="top-right-image" />
    </div>








  <img src="https://themewagon.github.io/pinwheel/images/icons/feature-shape.svg" alt="left Decoration"
  class="left-right-image" />
  <div class="container">
  <div class="first">
  <div class="h11">
    <h2 class="title">The Highlighting Part Of Our Solution</h2>
</div>
<div class="p11">
    <p class="description">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi egestas Werat viverra id et aliquet. vulputate egestas sollicitudin .
    </p>
</div>
</div>
    <div class="grid">
      <div v-for="(feature, index) in features" :key="index" class="card">
        <h3 class="card-title">{{ feature.title }}</h3>
        <p class="card-description">Lorem ipsum dolor sit amet consectetur, adipisicing elit.</p>
        <div class="icon" v-html="feature.icon"></div>
      </div>
    </div>
  </div>
</template>



// <script setup>
const features = [
  { title: "Live Caption", icon: "\u{1F4FA}" },
  { title: "Smart Reply", icon: "\u{1F4CE}" },
  { title: "Sound Amplifier", icon: "\u{1F514}" },
  { title: "Gesture Navigation", icon: "\u{1F4D0}" },
  { title: "Dark Theme", icon: "\u{1F4A1}" },
  { title: "Privacy Controls", icon: "\u{25B6}" },
  { title: "Location Controls", icon: "\u{1F4CD}" },
  { title: "Security Updates", icon: "\u{1F512}" },
  { title: "Focus Mode ", icon: "\u{1F512}" },
  { title: "Family Link", icon: "\u{1F512}" }
];
</script>


<style scoped>
/* body {
    font-family: "Arial", sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f9f9f9;
} */

/* Hero Section Styles */
.hero {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 50px 20px;
    font-family: Merriweather, sans-serif;
    color: white;
}

.content {
    max-width: 50%;
    padding-left: 25px;
    
}

.content h1 {
    font-family: Merriweather, sans-serif;
    font-size: 50px;
    margin-bottom: 20px;
    color: black;
    padding-right: 100px
}
.content p {
    font-size: 18px;
    margin-bottom: 20px;
    color: grey;
    font-family:  sans-serif;
    padding-right: 50px;
    line-height: 30px;
    padding-bottom: 30px;
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
    max-width: 625px;
    border-radius: 10px;
    padding-top: 30px;
    padding-right: 40px;
}

.top-right-image {
  position: absolute;
  top: -8rem;
  right: 0rem;
  width: 400px;
  z-index: -1;
}

/* Responsive Styles */
@media (max-width: 768px) {
    .hero {
        flex-direction: column;
        /* Stack the content and image vertically */
        align-items: center;
        text-align: center;
        padding: 0px;
        padding-top: 30px;
    }

    .content {
        max-width: 90%;
        /* Adjust the width of the content for smaller screens */
        text-align: left;
        padding: 0px;
    }

   .content h1 {
        font-size: 37px;
        /* Reduce the font size for the heading */
        padding: 0px;
    }

   .content p {
        font-size: 17px;
        /* Reduce the font size for the paragraph */
        padding: 0px;
    }

    .chart img {
        max-width: 90%;
        /* Make the image responsive to the screen size */
        margin-top: 20px;
        /* Add spacing between the content and the image */
        padding: 0px;
    }

    .theme-btn {
        width: 210px;
        /* Adjust button width for smaller screens */
        margin: 30px auto;
        /* Center the button */
    }
}

@media (max-width: 480px) {
    h1 {
        font-size: 24px;
        /* Further reduce the font size for very small screens */
    }

    p {
        font-size: 12px;
        /* Further reduce the paragraph font size */
    }

    .theme-btn {
        height: 40px;
        /* Adjust button height */
        font-size: 14px;
        /* Adjust button text size */
    }
}






.container {
  padding: 20px;
 
  text-align: center;
  padding-bottom: 150px;
}
.first{
    display: flex;
    justify-content:space-between;
    height:150px;
}
/* .h11{
    width: 50%;
} */
.title {
  font-size: 45px;
  font-weight: bold;
  color: #333;

padding-left: 30px;
text-align: left;

}
/* .p11{
    width: 50%;
} */
.description {
  color: #666;
  margin-top: 20px;
 
 padding-left: 130px;
line-height: 30px;
  text-align: left;
  font-size: 20px;
}

.grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 30px;
  transition: transform 0.2s ease;
  margin-top: 20px;
}

.card {
  background: white;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  text-align: left;
}
.card h3{
    font-size: 30px;
    padding-bottom: 10px;
}
.card p{
    font-size: 18px;
}
.icon {
  font-size: 24px;
  color: #e91e63;
  margin-bottom: 10px;
}

.card-title {
  font-size: 18px;
  font-weight: bold;
  color: #333;
}

.card-description {
  color: #666;
  margin-top: 5px;
}

@media (max-width: 768px) {
  .grid {
    grid-template-columns: repeat(2, 1fr);
    flex-direction: column;
    gap: 1.75rem;
  }
  .card {
  background: white;
  
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  text-align: left;
}
.card h3{
    font-size: 20px;
    padding-bottom: 10px;
}
.card p{
    font-size: 18px;
}
.icon {
  font-size: 24px;
  color: #e91e63;
  margin-bottom: 10px;
}

  .first {
    flex-direction: column;
   padding-bottom: 120px;
  }
 
.title {
  font-size: 35px;
  font-weight: bold;
  color: #333;
  padding-left: 0px;
  text-align: center;
}

.description {
  color: #666;
  padding-left: 0px;
  font-size: 20px;
  text-align: center;
}
  
}

</style>