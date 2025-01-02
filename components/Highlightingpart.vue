<template>
  <img src="https://themewagon.github.io/pinwheel/images/icons/feature-shape.svg" alt="left Decoration"
    class="left-right-image" />
  <section class="highlighting-part">
    <div class="container">
      <div class="header">
        <div class="text-content">
          <h2 id="heading">The Highlighting Part Of Our Solution</h2>
        </div>
        <div class="title">
          <p id="para">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi egestas Werat viverra id et
            aliquet. vulputate egestas sollicitudin
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
  <section class="marvel">
    <div class="content2">
      <h1>Prevent failure from to impacting your reputation</h1>
      <p>
        Our platform helps you build secure onboarding authentication experiences that retain and engage your users. We
        build the infrastructure, you can.
      </p>
      <button class="theme-btn2"><img src="https://themewagon.github.io/pinwheel/images/icons/drop.svg" alt=""> Habit
        building essential choose habit</button><br>
      <button class="theme-btn2"><img src="https://themewagon.github.io/pinwheel/images/icons/brain.svg" alt=""> Get an
        overview of Habit Calendars.</button><br>
      <button class="theme-btn2"><img src="https://themewagon.github.io/pinwheel/images/icons/timer.svg" alt=""> Start
        building with Habitify platform</button><br>
    </div>
    <div class="chart2">
      <img src="https://themewagon.github.io/pinwheel/images/sells-by-country.png" alt="Chart Image" />
    </div>




  </section>
  <section class="marvel1">
    <div class="chart3">
      <img src="https://themewagon.github.io/pinwheel/images/collaboration.png" alt="Chart Image" />
    </div>
    <div class="content3">
      <h1>Accept payments any country in this whole universe</h1>
      <p>
        Donec sollicitudin molestie malesda. Donec sollitudin molestie malesuada. Mauris pellentesque nec, egestas non
        nisi. Cras ultricies ligula sed
      </p>
      <div class="l">
        <p class="line"><img src="https://themewagon.github.io/pinwheel/images/icons/checkmark-circle.svg" alt="">
          Supporting more than 119 country world</p>
        <p class="line"><img src="https://themewagon.github.io/pinwheel/images/icons/checkmark-circle.svg" alt=""> Open
          transaction with more than currencies</p>
        <p class="line"><img src="https://themewagon.github.io/pinwheel/images/icons/checkmark-circle.svg" alt="">
          Customer Service with 79 languages</p>
      </div>
    </div>
  </section>






  <section class="marvel2">
    <div class="content4">
      <h1>Accountability that works for you</h1>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi egestas Werat viverra id et aliquet. vulputate
        egestas sollicitudin .
      </p>
      <button class="theme-btn3">Know About us</button>
    </div>
    <div class="chart4">
      <iframe class="iframe_style" src="https://www.youtube.com/embed/g3-VxLQO7do?si=_avTHd2u1VyfHRz-"
        title="YouTube video player" frameborder="0"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
        referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

    </div>

  </section>
  <section>
    <div class="testimonial-section">
      <div class="ratings">
        <div class="rate1">
          <h2 class="title">Our customers have nice things to say about us</h2>
        </div>
        <div class="rate2">
          <p class="subtitle">{{ subtitle }}</p>
        </div>
      </div>
      <div class="testimonial-container">
        <div class="testimonial-wrapper" :style="sliderStyle">
          <div v-for="(testimonial, index) in testimonials" :key="index" class="testimonial-card">
            <div class="profile-image">
              <img :src="testimonial.image" :alt="testimonial.name">
            </div>
            <h3 class="name">{{ testimonial.name }}</h3>
            <p class="company">{{ testimonial.company }}</p>
            <p class="review">{{ testimonial.review }}</p>
            <div class="rating">
              <span v-for="star in 5" :key="star" class="star">
                <img src="https://themewagon.github.io/pinwheel/images/icons/star.svg" alt="">

              </span>
            </div>
          </div>
        </div>

        <div class="dots">
          <span v-for="(_, index) in testimonials" :key="index" :class="['dot', { active: currentSlide === index }]"
            @click="setSlide(index)"></span>
        </div>
      </div>
    </div>
  </section>





</template>







<script setup>
import { ref, computed, onMounted, onBeforeUnmount } from 'vue'

const testimonials = [
  {
    name: 'Courtney Henry',
    company: 'microsoft corp',
    image: 'https://themewagon.github.io/pinwheel/images/users/user-5.png',
    review: 'Our platform helps build secure onboarding authentica experiences & engage your users. We build .',
    rating: 4
  },
  {
    name: 'Ronald Richards',
    company: 'meta limited',
    image: 'https://themewagon.github.io/pinwheel/images/users/user-2.png',
    review: 'Our platform helps build secure onboarding authentica experiences & engage your users. We build .',
    rating: 4
  },
  {
    name: 'Bessie Cooper',
    company: 'apple inc ltd',
    image: 'https://themewagon.github.io/pinwheel/images/users/user-6.png',
    review: 'Our platform helps build secure onboarding authentica experiences & engage your users. We build .',
    rating: 4
  }
]

const currentSlide = ref(0)
const subtitle = ref('Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi egestas Werat viverra id et aliquet. vulputate egestas sollicitudin .')

const sliderStyle = computed(() => ({
  transform: `translateX(-${currentSlide.value * 100}%)`,
  transition: 'transform 0.5s ease-in-out'
}))

const setSlide = (index) => {
  currentSlide.value = index
}

let autoSlideInterval

const startAutoSlide = () => {
  autoSlideInterval = setInterval(() => {
    currentSlide.value = (currentSlide.value + 1) % testimonials.length
  }, 5000)
}

onMounted(() => {
  startAutoSlide()
})

onBeforeUnmount(() => {
  clearInterval(autoSlideInterval)
})

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
#para {
  text-align: left;
  font-size: 18px;
  margin-left: 100px;
}

#heading {
  font-size: 40px;
  margin-left: 30px;
  margin-right: 60px;
  font-family: Merriweather, sans-serif;
}

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
  color: black;
  margin-right: 20px;
}

.title {
  flex: 1;
  text-align: right;
}

.title h2 {
  font-weight: 400;
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



.marvel {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 50px 20px;
  color: white;
}

.content2 {
  max-width: 50%;
  padding-left: 50px;
  padding-right: 70px;
}

h1 {
  font-size: 35px;
  margin-bottom: 20px;

  color: black;
}

p {
  color: grey;
}

.theme-btn2 {
  padding: 10px 20px;
  background-color: white;
  color: #020202;
  border: none;
  cursor: pointer;
  height: 50px;
  font-size: 16px;
  width: 350px;

}

iframe {
  border-radius: 20px;
}

.chart2 img {
  /* max-width: 600px; */
  border-radius: 10px;
  width: 100%;

}

.chart2 {
  padding-right: 50px;
}

a {
  color: #020202;
  padding-bottom: 20px;
}





.marvel1 {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 50px 20px;
  color: white;
}

.content3 {
  max-width: 50%;
  padding-left: 40px;
}

h1 {
  font-size: 40px;
  margin-bottom: 20px;

  color: black;
}

.content3 p {
  font-size: 17px;
  margin-bottom: 10px;
  padding-right: 30px;
  color: grey;

}

iframe {
  width: 650px;
  height: 400px;
}

.chart3 img {
  max-width: 630px;
  border-radius: 20px;

  margin-left: 50px;

}

.chart3 {
  padding-right: 50px;
}

.l p.line {
  color: #000000;
  font-size: 17px;
  line-height: 15px;
}





.marvel2 {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 50px 20px;
  color: white;
}

.content4 {
  max-width: 50%;
  padding-left: 40px;

}

h1 {
  font-size: 40px;
  margin-bottom: 20px;
  font-family: Merriweather, sans-serif;
  color: black;
}

p {
  font-size: 20px;
  margin-bottom: 20px;
  padding-right: 30px;
  color: grey;


}

.theme-btn3 {
  padding: 10px 20px;
  background-color: white;
  color: #020202;
  border-radius: 50px;
  cursor: pointer;
  height: 50px;
  font-size: 15px;
  width: 200px;
  margin-bottom: 10px;
  border: none;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
}

.chart4 img {
  max-width: 500px;
  border-radius: 10px;


}

.chart4 {
  padding-right: 50px;
}

a {
  color: #020202;
  padding-bottom: 20px;
}

.side {
  display: flex;
  gap: 50px;
  margin-left: 20px;
  margin-right: 25px;
  background-image: linear-gradient(184.78deg, #fa709a 7.64%, #fee140 120.07%);
  height: 325px;
  color: white;
  border-top-left-radius: 20px;
  border-top-right-radius: 20px;
  border-bottom-right-radius: 80px;
  border-bottom-left-radius: 80px;
}

.side2 {
  margin-right: 55px;
  font-size: 30px;
  padding-left: 90px;
  color: white;
  width: 1400px;
  margin-top: 35px;
}

.side3 {
  color: white;
  margin-top: 35px;
  padding-right: 40px;
}

.button1 {
  padding: 10px 20px;
  background-color: white;
  border-radius: 50px;
  height: 50px;
  font-size: 15px;
  width: 200px;
  margin-bottom: 10px;
  border: none;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
}










.testimonial-section {
  padding: 2rem;
  max-width: 1200px;
  margin: 0 auto;

}

.title {
  font-size: 2rem;
  text-align: center;
  margin-bottom: 1rem;
}

.subtitle {
  text-align: center;
  color: #666;
  margin-bottom: 3rem;
}

.testimonial-container {
  overflow: hidden;
  position: relative;

}

.testimonial-wrapper {
  display: flex;
  width: 100%;
  width: 400px;
}

.testimonial-card {
  flex: 0 0 100%;
  padding: 2rem;
  text-align: center;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
  margin-right: 50px;
  border-radius: 20px;
}

.profile-image {
  width: 80px;
  height: 80px;
  border-radius: 50%;
  margin: 0 auto 1rem;
  overflow: hidden;
  border-style: solid;
  border-color: #de8f4a;
}

.profile-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;


}

.name {
  font-size: 1.2rem;
  margin-bottom: 0.5rem;
}

.company {
  color: #666;
  margin-bottom: 1rem;
}

.review {
  margin-bottom: 1rem;
}

.rating {
  color: #ffd700;
  margin-bottom: 1rem;
}

.dots {
  display: flex;
  justify-content: center;
  gap: 0.5rem;
  margin-top: 2rem;
  background-color: white;
}

.dot {
  width: 10px;
  height: 10px;
  border-radius: 50%;
  background-color: #ddd;
  cursor: pointer;
  transition: background-color 0.3s;
}

.dot.active {
  background-color: #ff6b6b;
}

.ratings {
  display: flex;
  margin-bottom: 90px;
  align-items: center;
}

.rate1 h2 {
  font-size: 40px;
  text-align: left;
}

.rate2 p {
  margin-left: 0 !important;
  font-size: 18px;
  padding-top: 20px;
  /* text-align: left; */

}

.iframe_style{
  height: 20rem;
  width: 40rem;
}

/* Responsive for smaller screens */
@media (max-width: 768px) {
  .iframe_style{
    height: 10rem;
    width: auto;
  }
  #heading {
    font-size: 28px;
  }
  .ratings{
    flex-direction: column;
  }

  #para {
    font-size: 16px;
    margin: 0 10px;
  }

  .header {
    flex-direction: column;
    text-align: left;
    gap: 10px;
  }

  .cards {
    grid-template-columns: 1fr;
    gap: 10px;
  }

  .card {
    padding: 10px;
  }

  .card h3 {
    font-size: 0.9rem;
  }

  .card p {
    font-size: 0.8rem;
  }

  .marvel,
  .marvel1,
  .marvel2 {
    flex-direction: column;
    text-align: center;
    padding: 20px 10px;
  }

  .content2,
  .content3,
  .content4 {
    max-width: 100%;
    padding: 0;
  }

  .chart2 img,
  .chart3 img,
  .chart4 img {
    max-width: 100%;
    height: auto;
  }

  .chart4 {
    height: 20rem;
    width: 100%;
  }

  .theme-btn2,
  .theme-btn3 {
    width: 90%;
    margin: 10px auto;
  }
}

@media (max-width: 576px) {
  h1 {
    font-size: 24px;
  }

  .title h2 {
    font-size: 1.5rem;
  }

  p {
    font-size: 0.9rem;
  }

  .testimonial-card {
    padding: 15px;
  }

  .profile-image {
    width: 60px;
    height: 60px;
  }

  .name {
    font-size: 1rem;
  }

  .dots {
    gap: 0.3rem;
  }

  .dot {
    width: 8px;
    height: 8px;
  }
}
</style>