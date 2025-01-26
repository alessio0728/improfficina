<template>

 
  <div class="book-container">
      <div class="book">
          <p>VINO 1 <br> 10€</p>
          
          <div class="cover">
              <img src="../media/vino 1.jpg" alt="vino">
          </div>
      </div>
  
      <div class="book">
          <p>VINO 1 <br> 10€</p>
          
          <div class="cover">
              <img src="../media/vino 2.jpg" alt="vino">
          </div>
      </div>
  
      <div class="book">
          <p>VINO 1 <br> 10€</p>
          
          <div class="cover">
              <img src="../media/vino 3.jpg" alt="vino">
          </div>
      </div>
  
      <!-- Aggiungi altri div .book come necessario -->
  
      <div class="book">
          <p>VINO 1 <br> 10€</p>
          
          <div class="cover">
              <img src="../media/vino 4.jpg" alt="vino">
          </div>
      </div>
  
      <!-- Aggiungi altri div .book come necessario -->
  
      <div class="book">
          <p>VINO 1 <br> 10€</p>
          
          <div class="cover">
              <img src="../media/vino 5.jpg" alt="vino">
          </div>
      </div>
  
      <!-- Aggiungi altri div .book come necessario -->
  
      <div class="book">
          <p>VINO 1 <br> 10€</p>
          
          <div class="cover">
              <img src="../media/vino 6.jpg" alt="vino">
          </div>
      </div>
  
      <!-- Aggiungi altri div .book come necessario -->
  
      <div class="book">
          <p>VINO 1 <br> 10€</p>
          
          <div class="cover">
              <img src="../media/vino 7.jpg" alt="vino">
          </div>
      </div>
  
      <!-- Aggiungi altri div .book come necessario -->
  
      <div class="book">
          <p>VINO 1 <br> 10€</p>
          
          <div class="cover">
              <img src="../media/vino 8.jpg" alt="vino">
          </div>
      </div>
  
  
  
  </div>
  </template>
  
  
  
  <style scoped>
  
  img{
      border-radius: 10px; 
      height: 100%;
  
  }
  
  .book-container {
              display: flex;
              flex-wrap: wrap; /* Permette ai div di andare a capo se non ci sono abbastanza spazi */
              gap: 20px; /* Spazio tra i div */
              justify-content: center;
              overflow-y: auto; /* Scroll verticale quando necessario */
              max-height: 100vh; 
          }
          
          @media (max-width: 768px) {
      .book-container {
          flex-wrap: wrap; /* Mantieni il wrapping su schermi medi */
          overflow-y: auto; /* Scroll verticale su schermi medi */
          max-height: 70vh; /* Limite di altezza su schermi medi */
      }
  }
          @media (max-width: 480px) {
              .book {
                  flex: 1 1 100%; /* 1 item per row on small screens */
              }
          }
  
  
  
  /* From Uiverse.io by eslam-hany */ 
  .book {
    position: relative;
    border-radius: 10px;
    width: 220px;
    height: 300px;
    background-color: whitesmoke;
    -webkit-box-shadow: 1px 1px 12px #000;
    box-shadow: 1px 1px 12px #000;
    -webkit-transform: preserve-3d;
    -ms-transform: preserve-3d;
    transform: preserve-3d;
    -webkit-perspective: 2000px;
    perspective: 2000px;
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-align: center;
    -ms-flex-align: center;
    align-items: center;
    -webkit-box-pack: center;
    -ms-flex-pack: center;
    justify-content: center;
    color: #000;
  }
  
  .cover {
    top: 0;
    position: absolute;
    background-color: lightgray;
    width: 100%;
    height: 100%;
    border-radius: 10px;
    cursor: pointer;
    -webkit-transition: all 0.5s;
    transition: all 0.5s;
    -webkit-transform-origin: 0;
    -ms-transform-origin: 0;
    transform-origin: 0;
    -webkit-box-shadow: 1px 1px 12px #000;
    box-shadow: 1px 1px 12px #000;
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-align: center;
    -ms-flex-align: center;
    align-items: center;
    -webkit-box-pack: center;
    -ms-flex-pack: center;
    justify-content: center;
  }
  
  .book:hover .cover {
    -webkit-transition: all 0.5s;
    transition: all 0.5s;
    -webkit-transform: rotatey(-80deg);
    -ms-transform: rotatey(-80deg);
    transform: rotatey(-80deg);
  }
  
  p {
    font-size: 20px;
    font-weight: bolder;
  }
  
  
  
  
  </style>