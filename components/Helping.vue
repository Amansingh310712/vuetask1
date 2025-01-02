<template>
    <div class="side">
      <div class="side2">
        <h2>Helping teams in the world with focus</h2>
        <button class="button1">Download the theme</button>
      </div>
      <div class="side3">
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi egestas
          Werat viverra id et aliquet. Vulputate egestas sollicitudin.
        </p>
      </div>
    </div>
  </template>
  
  <style>
  .side {
    display: flex;
    gap: 50px;
    margin: 0 50px;
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
  
  /* Mobile Responsive */
  @media (max-width: 768px) {
    .side {
      flex-direction: column;
      gap: 20px;
      height: auto;
      margin: 20px;
      padding: 20px;
      border-radius: 20px;
    }
  
    .side2 {
      font-size: 20px;
      padding-left: 20px;
      margin-right: 0;
      width: auto;
      text-align: center;
    }
  
    .side3 {
      margin-top: 0;
      padding-right: 20px;
      text-align: center;
    }
  
    .button1 {
      width: 150px;
      font-size: 14px;
    }
  }
  </style>