<template>
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
              <path d="..." fill="#222222"></path>
            </svg>
            <svg width="19" height="15" viewBox="0 0 19 15" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path d="..." fill="#222222"></path>
            </svg>
            <svg width="19" height="16" viewBox="0 0 19 16" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path d="..." fill="#222222"></path>
            </svg>
            <svg width="19" height="18" viewBox="0 0 17 18" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path d="..." fill="#222222"></path>
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
          <p>
            2118 Thornridge Cir. Syracuse, <br />
            Connecticut 35624 <br />
            (704) 555-0127
          </p>
        </div>
      </div>
      <div class="footer-bottom">
        <p class="last">Designed And Developed by Themefisher | Distributed by ThemeWagon</p>
      </div>
    </footer>
  </template>
  
  <style>
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
  }
  
  .container1 {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    gap: 20px;
  }
  
  .footer-section {
    flex: 1 1 250px;
    min-width: 200px;
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
    gap: 20px;
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
    color: grey;
    transition: color 0.3s;
  }
  
  .footer-section ul li a:hover {
    color: #de8f4a;
  }
  
  .footer-bottom p {
    text-align: center;
    font-size: 15px;
    color: #888;
    margin-top: 60px;
  }
  
  svg {
    background-color: white;
    height: 30px;
    width: 20px;
    border-radius: 50px;
  }
  
  /* Mobile Responsive */
  @media (max-width: 768px) {
    .container1 {
      flex-direction: column;
      align-items: center;
      gap: 30px;
    }
  
    .footer-section {
      text-align: center;
    }
  
    .footer-section h3 {
      font-size: 16px;
    }
  
    .footer-section p,
    .footer-section address {
      font-size: 13px;
    }
  
    .social-icons {
      justify-content: center;
    }
  
    .footer-bottom p {
      font-size: 13px;
    }
  }
  
  @media (max-width: 480px) {
    .footer {
      padding: 20px 10px;
    }
  
    .footer-section {
      flex: 1 1 100%;
    }
  
    .footer-section h3 {
      font-size: 14px;
    }
  
    .footer-section p {
      font-size: 12px;
    }
  }
  </style>