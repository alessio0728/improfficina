<template>

    <center>
    <div class="card">
      <div class="card-inner">
        <div class="card-front">
    
          <img src="../media/daniele.jpg" alt="Il proprietario Daniele Cirsone" >
    
        </div>
    
        <div class="card-back">
          <p>Vendo <u>SOLO</u> i miei vini preferiti selezionati in 16 anni di assaggi professionali.
    
            Oltre 30 vini in degustazione al calice. <br>
            
            Degustazioni fino alle 22.30 ogni venerdi 🍷 <br> <br>
    
            <center>Whatapp 3209072590</center>
          </p>
        </div>
      </div>
    </div>
    </center>
    
    </template>
    
    <style scoped>
    .card {
      width: 80%; /* Inizia con una larghezza del 80% per dispositivi più grandi */
      max-width: 500px; /* Imposta una larghezza massima per evitare che diventi troppo grande */
      height: 400px;
      perspective: 1000px;
      margin: 0 auto; /* Centra il card orizzontalmente */
    }
    
    .card-inner {
      width: 100%;
      height: 100%;
      position: relative;
      transform-style: preserve-3d;
      transition: transform 0.999s;
    }
    
    .card:hover .card-inner {
      transform: rotateY(180deg);
    }
    
    .card-front,
    .card-back {
      position: absolute;
      width: 100%;
      height: 100%;
      backface-visibility: hidden;
    }
    
    .card-front {
      color: #fff;
      display: flex;
      align-items: center;
      border-radius: 10px;
      justify-content: center;
      font-size: 24px;
      transform: rotateY(0deg);
    }
    
    .card-back {
      background-color: #F08A5D;
      color: #fff;
      display: flex;
      align-items: center;
      border: 10px solid #F08A5D;
      border-radius: 10px;
      justify-content: center;
      font-size: 24px;
      transform: rotateY(180deg);
    }
    
    /* Media query per dispositivi con schermi più piccoli */
    @media (max-width: 600px) {
      .card {
        width: 90%; /* Riduci la larghezza al 90% per schermi più piccoli */
        height: 300px; /* Riduci l'altezza per schermi più piccoli */
      }
    
      .card-front,
      .card-back {
        font-size: 18px; /* Riduci la dimensione del font per schermi più piccoli */
      }
    }
    </style>