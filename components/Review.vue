<script>
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
</script>







<template>
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
      <span 
        v-for="(_, index) in testimonials" 
        :key="index"
        :class="['dot', { active: currentSlide === index }]"
        @click="setSlide(index)"
      ></span>
    </div>
  </div>
</div>
</section>
</template>





<style>
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
.ratings{
  display: flex;
  margin-bottom: 90px;
  
}
.rate1 h2{
font-size: 40px;
text-align: left;
}
.rate2 p{
  margin-left: 300px;
  font-size: 18px;
  padding-top: 20px;
  text-align: left;
 
}

</style>