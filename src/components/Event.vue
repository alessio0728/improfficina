<template>
  <div class="flex flex-col items-center justify-center min-h-screen p-4">
    <!-- Immagine con meno spazio sopra -->
    <div class="mb-4 mt-[-20px]">
      <a target="_blank"
        href="https://www.eventbrite.it/e/biglietti-improlimpiadi-spettacolo-di-improvvisazione-teatrale-1221939005459?aff=oddtdtcreator&fbclid=IwY2xjawIHEW1leHRuA2FlbQIxMAABHbbpryupwnABUDHDGxfQjaybOv49BwqWsUffXRu9a2_avrZJAusbtRjKZw_aem_EVTVGhhgeom8AYvMMOYhAw">
        <img class="degustazione w-[300px] sm:w-[400px] md:w-[500px] lg:w-[60%] xl:w-[65%] mx-auto"
          src="/public/media/calendarioFebbraio2025.png" alt="degustazione" />
      </a>
    </div>

    <!-- Countdown -->
    <div class="grid grid-cols-2 md:grid-flow-col gap-5 text-center mb-8">
      <div class="countdown-box">
        <span class="countdown">{{ days }}</span>
        <span class="time">GIORNI</span>
      </div>
      <div class="countdown-box">
        <span class="countdown">{{ hours }}</span>
        <span class="time">ORE</span>
      </div>
      <div class="countdown-box">
        <span class="countdown">{{ minutes }}</span>
        <span class="time">MINUTI</span>
      </div>
      <div class="countdown-box">
        <span class="countdown">{{ seconds }}</span>
        <span class="time">SECONDI</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      days: 0,
      hours: 0,
      minutes: 0,
      seconds: 0,
      countdownInterval: null,
    };
  },
  mounted() {
    this.startCountdown();
  },
  beforeUnmount() {
    clearInterval(this.countdownInterval);
  },
  methods: {
    startCountdown() {
      const targetDate = new Date('2025-02-01T20:30:00Z');
      this.countdownInterval = setInterval(() => {
        const now = new Date();
        const diff = targetDate - now;

        if (diff <= 0) {
          clearInterval(this.countdownInterval);
          this.days = 0;
          this.hours = 0;
          this.minutes = 0;
          this.seconds = 0;
          alert('Evento finito! Ci vediamo alla prossima con nuovi vini!');
          return;
        }

        this.days = Math.floor(diff / (1000 * 60 * 60 * 24));
        this.hours = Math.floor((diff % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
        this.minutes = Math.floor((diff % (1000 * 60 * 60)) / (1000 * 60));
        this.seconds = Math.floor((diff % (1000 * 60)) / 1000);
      }, 1000);
    },
  },
};
</script>

<style scoped>

a{
  cursor: pointer;
}
.countdown {
  font-family: 'Courier New', Courier, monospace;
  font-size: 3rem;
  font-weight: bold;
  text-align: center;
  color: white;
}

.countdown-box {
  background-color: #2d3748;
  border-radius: 0.5rem;
  padding: 15px;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.time {
  color: white;
  font-size: 1rem;
  margin-top: 5px;
}
</style>