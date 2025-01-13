<template>
  <div class="flex flex-col items-center justify-center h-screen">
    <div class="mb-8">
      <img class="degustazione" src="../media/degustazione31102024.jpg" alt="degustazione" width="500px" />
    </div>
    
    <div class="grid auto-cols-max grid-flow-col gap-5 text-center mb-8">
      <div class="bg-neutral rounded-box text-neutral-content flex flex-col p-2">
        <span class="countdown font-mono text-5xl">
          {{ days }}
        </span>
        <span class="time">GIORNI</span>
      </div>
      <div class="bg-neutral rounded-box text-neutral-content flex flex-col p-2">
        <span class="countdown font-mono text-5xl">
          {{ hours }}
        </span>
        <span class="time">ORE</span>
      </div>
      <div class="bg-neutral rounded-box text-neutral-content flex flex-col p-2">
        <span class="countdown font-mono text-5xl">
          {{ minutes }}
        </span>
        <span class="time">MINUTI</span>
      </div>
      <div class="bg-neutral rounded-box text-neutral-content flex flex-col p-2">
        <span class="countdown font-mono text-5xl">
          {{ seconds }}
        </span>
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
      const targetDate = new Date('2025-01-18T20:30:00Z'); // Data corretta
      this.countdownInterval = setInterval(() => {
        const now = new Date();
        const diff = targetDate - now;

        if (diff <= 0) {
          clearInterval(this.countdownInterval);
          this.days = 0;
          this.hours = 0;
          this.minutes = 0;
          this.seconds = 0;
          alert('Evento finito ci vediamo alla prossima con nuovi vini!');
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
.countdown {
  font-family: 'Courier New', Courier, monospace;
  text-align: center;
  color: white;
}

.grid.auto-cols-max.grid-flow-col.gap-5.text-center.mb-8 {
  margin-bottom: 250px;
}

.bg-neutral {
  background-color: #2d3748;
  border-radius: 0.5rem;
  padding: 10px;
}

.time{
  color: white;
  
}
</style>