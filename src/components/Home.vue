<template>

  <div class="container">

    <figure> <img src="/public/media/logo.jpeg" alt="logo"></figure>

  </div>
  <div class="wrapper">
    <div class="marquee">
      <p>
        IL PROSSIMO EVENTO SARA' AL TEATRO OSSEVATORIO IL 01-02-2025 ORE 21:00 IN VIA GIUSEPPE RE DAVID, 116/A
      </p>
      <p>
        IL PROSSIMO EVENTO SARA' AL TEATRO OSSEVATORIO IL 01-02-2025 ORE 21:00 IN VIA GIUSEPPE RE DAVID, 116/A
      </p>
    </div>

  </div>

  <div>

    <div class="btn-container">
      <a target="_blank"
        href="https://www.eventbrite.it/e/biglietti-improlimpiadi-spettacolo-di-improvvisazione-teatrale-1221939005459?aff=oddtdtcreator&fbclid=IwY2xjawIHEW1leHRuA2FlbQIxMAABHbbpryupwnABUDHDGxfQjaybOv49BwqWsUffXRu9a2_avrZJAusbtRjKZw_aem_EVTVGhhgeom8AYvMMOYhAw">
        <button class="btn_prenota">PRENOTA QUI</button>
      </a>
    </div>


  </div>


</template>

<style scoped>
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  max-height: 70vh;
  padding: 0;/* Rimuove eventuali padding indesiderati */
}

.container figure {
  margin: 0;
}

.container img {
  max-width: 100%;
  height: auto;
}

/* Stile bottone */
.btn-container {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 20px;
  /* Regola la distanza tra il bottone e il testo */
}

.btn_prenota {
  background-color: white;
  color: black;
  font-size: 24px;
  padding: 15px 30px;
  border: 2px solid black;
  border-radius: 10px;
  cursor: pointer;
  font-weight: bold;
  text-transform: uppercase;
  transition: background-color 0.3s ease, transform 0.2s ease;
}

.btn_prenota:hover {
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

p {
  color: white;
  padding-left: 10px;
  font-weight: bold;
  font-size: xx-large;
  margin-bottom: 30px;
  z-index: 1;
  margin-bottom: 10px;
  /* Riduci lo spazio sotto l'immagine */

}

.wrapper {
  max-width: 100%;
  overflow: hidden;
  margin-top: -50px;
  /* Avvicina il testo all'immagine */
}

.marquee {
  white-space: nowrap;
  overflow: hidden;
  display: inline-block;
  animation: marquee 15s linear infinite;
}

.marquee p {
  display: inline-block;
}

@keyframes marquee {
  0% {
    transform: translate3d(0, 0, 0);
  }

  100% {
    transform: translate3d(-50%, 0, 0);
  }
}
</style>