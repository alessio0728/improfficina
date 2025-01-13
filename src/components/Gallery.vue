<template>

    <div class="galleria">
      <figure class="galleria__elemento ">
        <img
          src="../media/galleria 7.jpg"
          alt="Immagine della galleria 1"
          class="galleria__immagine"
        />
      </figure>
    
      <figure class="galleria__elemento ">
        <img
          src="../media/galleria 2.jpg"
          alt="Immagine della galleria 2"
          class="galleria__immagine"
        />
      </figure>
    
      <figure class="galleria__elemento ">
        <img
          src="../media/galleria 3.jpg"
          alt="Immagine della galleria 3"
          class="galleria__immagine"
        />
      </figure>
    
      <figure class="galleria__elemento ">
        <img
          src="../media/galleria 4.jpg"
          alt="Immagine della galleria 4"
          class="galleria__immagine"
        />
      </figure>
    
      <figure class="galleria__elemento ">
        <img
          src="../media/galleria 5.jpg"
          alt="Immagine della galleria 5"
          class="galleria__immagine"
        />
      </figure>
    
      <figure class="galleria__elemento ">
        <img
          src="../media/galleria 6.jpg"
          alt="Immagine della galleria 6"
          class="galleria__immagine"
        />
      </figure>
    
      <figure class="galleria__elemento ">
        <img
          src="../media/galleria 8.jpg"
          alt="Immagine della galleria 6"
          class="galleria__immagine"
        />
      </figure>
    
      <figure class="galleria__elemento ">
        <img
          src="../media/galleria 9.jpg"
          alt="Immagine della galleria 6"
          class="galleria__immagine"
        />
      </figure>
    
      <figure class="galleria__elemento ">
        <img
          src="../media/galleria 10.jpg"
          alt="Immagine della galleria 6"
          class="galleria__immagine"
        />
      </figure>
    
      <figure class="galleria__elemento ">
        <img
          src="../media/galleria 11.jpg"
          alt="Immagine della galleria 6"
          class="galleria__immagine"
        />
      </figure>
    
      <figure class="galleria__elemento ">
        <img
          src="../media/galleria 12.jpg"
          alt="Immagine della galleria 6"
          class="galleria__immagine"
        />
      </figure>
    
      <figure class="galleria__elemento ">
        <img
          src="../media/galleria 13.jpg"
          alt="Immagine della galleria 6"
          class="galleria__immagine"
        />
      </figure>
    
      <figure class="galleria__elemento ">
        <img
          src="../media/galleria 14.jpg"
          alt="Immagine della galleria 6"
          class="galleria__immagine"
        />
      </figure>
    
      <figure class="galleria__elemento ">
        <img
          src="../media/galleria 15.jpg"
          alt="Immagine della galleria 6"
          class="galleria__immagine"
        />
      </figure>
    
      <figure class="galleria__elemento ">
        <img
          src="../media/galleria 16.jpg"
          alt="Immagine della galleria 6"
          class="galleria__immagine"
        />
      </figure>
    
      <figure class="galleria__elemento ">
        <img
          src="../media/galleria 17.jpg"
          alt="Immagine della galleria 6"
          class="galleria__immagine"
        />
      </figure>
    
      <figure class="galleria__elemento ">
        <img
          src="../media/galleria 18.jpg"
          alt="Immagine della galleria 6"
          class="galleria__immagine"
        />
      </figure>
    
      <figure class="galleria__elemento ">
        <img
          src="../media/galleria 19.jpg"
          alt="Immagine della galleria 6"
          class="galleria__immagine"
        />
      </figure>
    
      <figure class="galleria__elemento ">
        <img
          src="../media/galleria 20.jpg"
          alt="Immagine della galleria 6"
          class="galleria__immagine"
        />
      </figure>
    
    </div>
    
    </template>
    
    <style scoped>
    
    .galleria {
        display: grid;
        grid-template-columns: repeat(4, 1fr); /* 4 colonne */
        grid-template-rows: repeat(4, 20vw); /* 4 righe con altezza del 20% della viewport */
        grid-gap: 20px;
        row-gap: 60px;
    }
    
    .image-container {
        overflow: hidden;
        border-radius: 10px;
        
    }
    
    .image-container img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        border-radius: 10px;
    }
    
    
    @media (max-width: 768px) {
      .galleria {
        grid-template-columns: repeat(2, 1fr); /* 2 colonne su schermi medi */
        grid-template-rows: repeat(8, 25vw); /* 8 righe con altezza del 25% della viewport */
        row-gap: 80px;
        max-height: 70vh;
        overflow-y: auto;
      }
    }
    </style>