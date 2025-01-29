<template>
  <div class="container">
    <div class="row justify-content-center">
      <div class="col-md-6 col-lg-4 mb-4">
        <div class="card h-100 d-flex flex-column">
          <img src="/public/media/maestro ian.jpg" class="card-img" alt="Maestro Ian">
          <div class="card-body d-flex flex-column">
            <h5 class="card-title">MAESTRO IAN ALGIE</h5>
            <p class="card-text">Descrizione breve del maestro Ian e il suo contributo.</p>
            <p class="card-text mt-auto"><small class="text-muted">Ultimo aggiornamento 3 minuti fa</small></p>
          </div>
        </div>
      </div>

      <div class="col-md-6 col-lg-4 mb-4">
        <div class="card h-100 d-flex flex-column">
          <img src="/public/media/maestro francesco.jpeg" class="card-img" alt="Maestro Francesco">
          <div class="card-body d-flex flex-column">
            <h5 class="card-title">Maestro Francesco</h5>
            <p class="card-text">Descrizione breve del maestro Francesco e il suo contributo. dgfdgdhtgdhhgtdhttghdhdrfhfdhfhhdhgrehygfyrfgsrygreygshyerghygfhuslohfughysubreyghasbfraybnuHARAH</p>
            <p class="card-text mt-auto"><small class="text-muted">Ultimo aggiornamento 3 minuti fa</small></p>
          </div>
        </div>
      </div>

      <div class="col-md-6 col-lg-4 mb-4">
        <div class="card h-100 d-flex flex-column">
          <img src="/public/media/maestra Angela.jpeg" class="card-img" alt="Maestra Angela" >
          <div class="card-body d-flex flex-column">
            <h5 class="card-title">Maestra Angela</h5>
            <p class="card-text">Descrizione breve della maestra Angela e il suo contributo.</p>
            <p class="card-text mt-auto"><small class="text-muted">Ultimo aggiornamento 3 minuti fa</small></p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>

.card-img {
  width: 100%;
  height: 60vh; /* Imposta un'altezza fissa */
  object-fit: cover; /* Ritaglia l'immagine senza distorsioni */
  transition: transform 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
}

.card:hover {
  background: linear-gradient(
    45deg,
    #FF0000, #FF7300, #FFFB00, #48FF00,
    #00FFD5, #002BFF, #FF00C8, #FF0000
  );
  transform: scale(1.05);
  box-shadow: 0px 0px 15px 5px rgba(255, 115, 0, 0.8),
              0px 0px 25px 10px rgba(0, 255, 213, 0.6);
  transition: all 0.3s ease-in-out;
}



</style>