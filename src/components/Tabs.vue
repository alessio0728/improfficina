<script setup>
import { ref } from 'vue';
import Home from './Home.vue';
import Products from './Info.vue';
import Boss from './Corsi.vue';
import Gallery from './Gallery.vue';
import Event from './Event.vue';

let tab = ref(0);
</script>

<template>
  <!-- Navbar -->
  <nav class="navbar navbar-dark bg-dark ">
    <div class="container-fluid"> 
      <a @click="tab=0" class="navbar-brand" href="#"><span class="title">IMPROFFICINA</span> </a>
      <button class="navbar-toggler" type="button" data-bs-toggle="offcanvas" data-bs-target="#offcanvasDarkNavbar" aria-controls="offcanvasDarkNavbar" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="offcanvas offcanvas-end text-bg-dark" tabindex="-1" id="offcanvasDarkNavbar" aria-labelledby="offcanvasDarkNavbarLabel">
        <div class="offcanvas-header">
          <h5 class="offcanvas-title" id="offcanvasDarkNavbarLabel">Dark offcanvas</h5>
          <button type="button" class="btn-close btn-close-white" data-bs-dismiss="offcanvas" aria-label="Close"></button>
        </div>
        <div class="offcanvas-body">
          <ul class="navbar-nav justify-content-end flex-grow-1 pe-3">
            <li @click="tab=0" class="nav-item"><span class="btn">HOME</span></li>
            <li @click="tab=2" class="nav-item"><span class="btn">INFO</span></li>
            <li @click="tab=3" class="nav-item"><span class="btn">CORSI</span></li>
            <li @click="tab=4" class="nav-item"><span class="btn">GALLERIA</span></li>
            <li @click="tab=5" class="nav-item"><span class="btn">EVENTI</span></li>
          </ul>
        </div>
      </div>
    </div>
  </nav>

  <!-- Contenuto -->
  <div class="py-4 px-6">
    <div v-if="tab === 0">
      <Home />
    </div>
    <div v-if="tab === 2">
      <Products />
    </div>
    <div v-if="tab === 3">
      <Boss />
    </div>
    <div v-if="tab === 4">
      <Gallery />
    </div>
    <div v-if="tab === 5">
      <Event />
    </div>
  </div>
</template>

<style scoped>
.py-10 {
  padding-top: 80px; /* Compensa l'altezza della navbar */
}

.nav-item {
  cursor: pointer;
  color: white;
  padding: 10px;
}

.nav-item.active {
  font-weight: bold;
  color: #0d6efd;
}

.title{
  display: flex ;
  justify-content: center;
  text-align: center;
  font-weight: 900;
  font-size: xx-large;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  text-shadow: 4px 4px 4px #dc0d0d;
}

.btn {
  margin: 10px;
  padding: 15px 40px;
  border: none;
  outline: none;
  color: #FFF;
  cursor: pointer;
  position: relative;
  z-index: 0;
  border-radius: 12px;
}
.btn::after {
  content: "";
  z-index: -1;
  position: absolute;
  width: 100%;
  height: 100%;
  background-color: #333;
  left: 0;
  top: 0;
  border-radius: 10px;
}
/* glow */
.btn::before {
  content: "";
  background: linear-gradient(
    45deg,
    #FF0000, #FF7300, #FFFB00, #48FF00,
    #00FFD5, #002BFF, #FF00C8, #FF0000
  );
  position: absolute;
  top: -2px;
  left: -2px;
  background-size: 600%;
  z-index: -1;
  width: calc(100% + 4px);
  height:  calc(100% + 4px);
  filter: blur(8px);
  animation: glowing 20s linear infinite;
  transition: opacity .3s ease-in-out;
  border-radius: 10px;
  opacity: 0;
}

@keyframes glowing {
  0% {background-position: 0 0;}
  50% {background-position: 400% 0;}
  100% {background-position: 0 0;}
}

/* hover */
.btn:hover::before {
  opacity: 1;
}

.btn:active:after {
  background: transparent;
}

.btn:active {
  color: #000;
  font-weight: bold;
}
</style>




