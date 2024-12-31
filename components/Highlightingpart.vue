<template>
  <section class="highlighting-part">
    <div class="container">
      <div class="header">
        <div class="text-content">
          <h2 id="heading">The Highlighting Part Of Our Solution</h2>
        </div>
        <div class="title">
          <p id="para">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi egestas Werat viverra id et aliquet. vulputate egestas sollicitudin              
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
          Our platform helps you build secure onboarding authentication experiences that retain and engage your users. We build the infrastructure, you can.
        </p>
        <button class="theme-btn2"><img src="https://themewagon.github.io/pinwheel/images/icons/drop.svg" alt="">     Habit building essential choose habit</button><br>
        <button class="theme-btn2"><img src="https://themewagon.github.io/pinwheel/images/icons/brain.svg" alt="">     Get an overview of Habit Calendars.</button><br>
        <button class="theme-btn2"><img src="https://themewagon.github.io/pinwheel/images/icons/timer.svg" alt="">      Start building with Habitify platform</button><br>
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
          Donec sollicitudin molestie malesda. Donec sollitudin molestie malesuada. Mauris pellentesque nec, egestas non nisi. Cras ultricies ligula sed
        </p>
        <div class="l">
          <p class="line"><img src="https://themewagon.github.io/pinwheel/images/icons/checkmark-circle.svg" alt="">   Supporting more than 119 country world</p>
        <p class="line"><img src="https://themewagon.github.io/pinwheel/images/icons/checkmark-circle.svg" alt="">      Open transaction with more than currencies</p>
        <p class="line"><img src="https://themewagon.github.io/pinwheel/images/icons/checkmark-circle.svg" alt="">     Customer Service with 79 languages</p>
        </div>
      </div>
    </section>






    <section class="marvel2">
      <div class="content4">
        <h1>Accountability that works for you</h1>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi egestas Werat viverra id et aliquet. vulputate egestas sollicitudin .
        </p>
        <button class="theme-btn3">Know About us</button>
      </div>
      <div class="chart4">
        <iframe width="560" height="315" src="https://www.youtube.com/embed/g3-VxLQO7do?si=_avTHd2u1VyfHRz-" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
        
      </div>
      
    </section>
    <section>
    <div class="testimonial-section">
    <div>
  <h2 class="title">Our customers have nice things to say about us</h2>
  <p class="subtitle">{{ subtitle }}</p>
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
            ⭐
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


    <div class="side">
        <div class="side2">
          <h2>Helping teams in the world with focus</h2>
          <button class="button1">dowload the theme</button>
        </div>
        <div class="side3">
          <p class="side3">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi egestas
            Werat viverra id et aliquet. Vulputate egestas sollicitudin.
          </p>
        </div>
    </div>
    <footer class="footer">
  <div class="container1">
    <div class="footer-section">
      <img src="https://themewagon.github.io/pinwheel/images/logo.svg" alt="Pinewheel logo" />
      <p>Lorem ipsum dolor sit sed dmi amet, consectetur adipiscing. Cdo tellus, sed condimentum volutpat.</p>
    </div>
    <div class="footer-section">
      <h3>Socials</h3>
      <p>themefisher@gmail.com</p>
      <div class="social-icons">
        <svg width="19" height="21" viewBox="0 0 20 21" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path d="M19.1056 10.4495C19.1056 5.09642 15 0.759277 9.9327 0.759277C4.86539 0.759277 0.759766 5.09642 0.759766 10.4495C0.759766 15.2946 4.08865 19.3191 8.49018 20.0224V13.2627H6.15996V10.4495H8.49018V8.33951C8.49018 5.91696 9.85872 4.54939 11.93 4.54939C12.9657 4.54939 14.0013 4.74476 14.0013 4.74476V7.12823H12.8547C11.7081 7.12823 11.3382 7.87063 11.3382 8.65209V10.4495H13.8904L13.4835 13.2627H11.3382V20.0224C15.7398 19.3191 19.1056 15.2946 19.1056 10.4495Z" fill="#222222"></path>
            </svg> 
            <svg width="19" height="15" viewBox="0 0 19 15" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path d="M16.3308 3.92621C17.0129 3.42889 17.6269 2.83209 18.1044 2.13583C17.4904 2.40108 16.7742 2.60001 16.0579 2.66632C16.8083 2.2353 17.354 1.5722 17.6269 0.743317C16.9447 1.14118 16.1603 1.43958 15.3758 1.60535C14.6937 0.909093 13.7728 0.51123 12.7496 0.51123C10.7714 0.51123 9.16837 2.06952 9.16837 3.99252C9.16837 4.25777 9.20248 4.52301 9.27069 4.78825C6.3034 4.62247 3.64307 3.22995 1.86952 1.14118C1.56256 1.63851 1.39202 2.2353 1.39202 2.8984C1.39202 4.09199 2.00595 5.15296 2.99504 5.7829C2.41523 5.74975 1.83541 5.61713 1.35792 5.35189V5.38504C1.35792 7.07596 2.58576 8.46847 4.22289 8.80002C3.95003 8.86633 3.60897 8.93265 3.302 8.93265C3.06326 8.93265 2.85862 8.89949 2.61987 8.86633C3.06326 10.2589 4.39342 11.2535 5.96233 11.2867C4.73449 12.215 3.19968 12.7786 1.52845 12.7786C1.22149 12.7786 0.948636 12.7455 0.675781 12.7123C2.24469 13.707 4.12057 14.2706 6.16698 14.2706C12.7496 14.2706 16.3308 8.99896 16.3308 4.39039C16.3308 4.22461 16.3308 4.09199 16.3308 3.92621Z" fill="#222222"></path>
            </svg>
            <svg width="19" height="16" viewBox="0 0 19 16" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path d="M4.56609 15.2704V5.45315H0.948103V15.2704H4.56609ZM2.73764 4.1398C3.90474 4.1398 4.83841 3.31895 4.83841 2.33394C4.83841 1.38176 3.90474 0.59375 2.73764 0.59375C1.60945 0.59375 0.675781 1.38176 0.675781 2.33394C0.675781 3.31895 1.60945 4.1398 2.73764 4.1398ZM18.0654 15.2704H18.1044V9.8857C18.1044 7.259 17.4041 5.22331 13.7472 5.22331C11.9966 5.22331 10.8295 6.04415 10.3237 6.79933H10.2848V5.45315H6.82246V15.2704H10.4404V10.411C10.4404 9.13053 10.7128 7.91568 12.5801 7.91568C14.4475 7.91568 14.4864 9.36036 14.4864 10.5095V15.2704H18.0654Z" fill="#222222"></path>
            </svg>
            <svg width="19" height="18" viewBox="0 0 17 18" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path d="M15.3829 10.554C15.4875 10.0381 15.5573 9.48523 15.5573 8.9324C15.5573 4.76772 12.3483 1.37701 8.40687 1.37701C7.88367 1.37701 7.36047 1.45072 6.87215 1.56129C6.20943 1.00846 5.37231 0.676758 4.50031 0.676758C2.33775 0.676758 0.59375 2.55639 0.59375 4.80458C0.59375 5.76282 0.87279 6.64735 1.39599 7.34761C1.29135 7.86359 1.22159 8.41642 1.22159 8.9324C1.22159 13.1339 4.43055 16.5246 8.37199 16.5246C8.89518 16.5246 9.41838 16.4509 9.9067 16.3404C10.5694 16.8932 11.4065 17.188 12.2785 17.188C14.4411 17.188 16.1851 15.3453 16.1851 13.0602C16.22 12.1388 15.9061 11.2543 15.3829 10.554ZM8.61615 13.9447C6.31407 13.9447 4.39567 12.8759 4.39567 11.5491C4.39567 10.9595 4.70959 10.4066 5.44207 10.4066C6.52335 10.4066 6.62799 12.0651 8.51151 12.0651C9.3835 12.0651 9.97646 11.6597 9.97646 11.1069C9.97646 10.4066 9.41838 10.2961 8.51151 10.0749C6.34895 9.48523 4.39567 9.2641 4.39567 6.86849C4.39567 4.65716 6.45359 3.84633 8.19759 3.84633C10.116 3.84633 12.0693 4.65716 12.0693 5.91024C12.0693 6.53679 11.6856 7.08962 11.0229 7.08962C10.0462 7.08962 10.0113 5.83653 8.40687 5.83653C7.49999 5.83653 6.94191 6.09452 6.94191 6.68421C6.94191 7.38446 7.67439 7.45818 9.34862 7.90044C10.7787 8.23214 12.5227 8.85869 12.5227 10.7383C12.5227 12.9128 10.5345 13.9447 8.61615 13.9447Z" fill="#222222"></path>
            </svg>
      </div>
    </div>
    <div class="footer-section">
      <h3>Quick Links</h3>
      <ul>
        <li><a href="#">About</a></li>
        <li><a href="#">Category</a></li>
        <li><a href="#">Testimonial</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </div>
    <div class="footer-section">
      <h3>Location & Contact</h3>
      
       <p> 2118 Thornridge Cir. Syracuse, <br>
        Connecticut 35624 <br>
        (704) 555-0127</p>
      
    </div>
  </div>
  <div class="footer-bottom">
    <p class="last">Designed And Developed by Themefisher | Distributed by ThemeWagon</p>
  </div>
</footer>

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
#para{
text-align: left;
font-size: 18px;
margin-left: 100px;
}
#heading{
font-size:40px;
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
  color:black;
  margin-right: 20px;
}

.title {
  flex:1;
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

  color:black;
}

p {
  color:grey;
}

.theme-btn2 {
  padding: 10px 20px;
  background-color:white;
  color: #020202;
  border: none;
  cursor: pointer;
  height: 50px;
  font-size: 16px;
  width: 350px;
  
}
iframe{
  border-radius: 20px;
}
.chart2 img {
  max-width: 600px;
  border-radius: 10px;
 

}
.chart2{
  padding-right: 50px;
}
a{
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

  color:black;
}

.content3 p {
  font-size: 17px;
  margin-bottom: 10px;
  padding-right: 30px;
  color:grey;

}
iframe{
 width :650px; 
  height :400px;
}
.chart3 img {
  max-width: 630px;
  border-radius: 20px;
 
  margin-left: 50px;

}
.chart3{
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
  color:black;
}

p {
  font-size: 20px;
  margin-bottom: 20px;
  padding-right: 30px;
  color:grey;
  

}

.theme-btn3 {
  padding: 10px 20px;
  background-color: white;
  color: #020202;
  border-radius:50px ;
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
.chart4{
  padding-right: 50px;
}
a{
  color: #020202;
 padding-bottom: 20px;
}
.side{
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
.side2{
margin-right: 55px;
font-size: 30px;
padding-left: 90px;
color: white;
width :1400px;
margin-top: 35px;
}
.side3{
  color: white;
  margin-top: 35px;
  padding-right: 40px;
}
.button1{
  padding: 10px 20px;
  background-color: white;
  border-radius:50px ;
  height: 50px;
  font-size: 15px;
  width: 200px;
  margin-bottom: 10px;
  border: none;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
}




body {
font-family: Arial, sans-serif;
margin: 0;
padding: 0;
}

.footer {
background-color: #f4f4f4;
padding: 40px 20px;
color: #333;
margin-top: 100px;
height: 250px;
padding-top: 80px;
}

.container1 {
display: flex;
flex-wrap: wrap;
justify-content: space-between;
gap: 20px;
}

.footer-section {
flex: 1 1 250px;
}

.logo {
font-size: 24px;
color: #000;
margin-bottom: 10px;
}

.footer-section h3 {
font-size: 18px;
margin-bottom: 10px;
}

.footer-section p,
.footer-section address {
font-size: 14px;
line-height: 1.6;

}

.social-icons {
display: flex;
gap: 25px;
}



.footer-section ul {
list-style: none;
padding: 0;
}

.footer-section ul li {
margin-bottom: 5px;
}

.footer-section ul li a {
text-decoration: none;
color:grey;
transition: color 0.3s;
}

.footer-section ul li a:hover {
color: #de8f4a;
}


.footer-bottom p{
text-align: center;
font-size: 15px;
color: #888;
margin-top: 60px;
}
svg{
background-color: white;
height: 40px;
width: 40px;
border-radius: 50px;
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
}

.testimonial-card {
flex: 0 0 100%;
padding: 2rem;
text-align: center;
}

.profile-image {
width: 80px;
height: 80px;
border-radius: 50%;
margin: 0 auto 1rem;
overflow: hidden;
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
</style>
