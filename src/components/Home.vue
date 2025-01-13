<template>

    <div >
    
        <h1 class="text animate__animated animate__zoomIn animate__delay-2s">330 Vini è un’enoteca <br>
            innovativa situata in <br>
             via Putignani 165 <br>
             che si propone di diventare un centro di <br>
              sviluppo della cultura del buon bere.</h1>
    </div>
    
    <div class="avatar">
      <div class="ring-primary ring-offset-base-100 w-24 rounded-full ring ring-offset-2 bg-yellow bg-yellow-300 ">
        <p class="text2 animate__animated animate__zoomIn ">Questo negozio non è solo un negozio</p>
      </div>
    </div>
    
    </template>
    
    <style>
    
    @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@700&display=swap');
    
    
    .text {
      color: yellow;
      text-align: center;
      font-family: 'Montserrat', sans-serif; /* Usa il font importato */
      font-weight: 700; /* Grassetto */
      font-size: 50px; /* Aumenta la dimensione del testo se necessario */
      margin-top: 50px;
      
    }
    
    .avatar {
      position: absolute;
      top: 90%;
      right: 20px;
      transform: translateY(-50%);
      
    }
    
    .text2{
        text-align: center;
        font-size: medium;
    }
    
    .ring-primary {
      --tw-ring-color: #3b82f6; /* Colore del bordo */
    }
    
    .ring-offset-base-100 {
      --tw-ring-offset-color: #ffffff; /* Colore dell'offset del bordo */
    }
    
    .w-24 {
      width: 6rem; /* Dimensione dell'immagine */
    }
    
    .rounded-full {
      border-radius: 9999px; /* Bordo arrotondato */
    }
    
    .ring {
      box-shadow: 0 0 0 calc(2px + var(--tw-ring-offset-width)) var(--tw-ring-color); /* Effetto bordo */
    }
    
    .ring-offset-2 {
      --tw-ring-offset-width: 2px; /* Spessore dell'offset del bordo */
    }
    
    @media (max-width: 760px) {
      .text{
        color: white;
        font-size: 30px;
      }
    
      .avatar{
        display: none;
      }
    }
    </style>