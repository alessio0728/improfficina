<template>
  <section class="container">
    <div class="card-grid">
      <a class="card" v-for="(image, index) in images" :key="index" @click="openModal(image)">
        <div :class="['background']" :style="{ backgroundImage: `url(${image})` }"></div>
      </a>
    </div>

    <!-- Modal -->
    <div v-if="modalOpen" class="modal-overlay" @click="closeModal">
      <div class="modal-content" @click.stop>
        <img :src="selectedImage" alt="Full screen image" />
        <button class="close-button" @click="closeModal">X</button>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      modalOpen: false,
      selectedImage: '',
      images: [
        '/media/impro1.jpeg',
        '/media/impro2.jpeg',
        '/media/impro3.jpeg',
        '/media/impro4.jpeg',
        '/media/impro5.jpeg',
        '/media/impro6.jpeg',
        '/media/impro7.jpeg',
        '/media/impro8.jpeg',
        '/media/impro9.jpeg',
        '/media/impro10.jpeg',
        '/media/impro11.jpeg',
        '/media/impro12.jpeg',
        '/media/impro13.jpeg',
        '/media/impro14.jpeg',
        '/media/impro15.jpeg',
        '/media/impro16.jpeg',
        '/media/impro17.jpeg',
        '/media/impro18.jpeg',
        '/media/impro19.jpeg',
        '/media/impro20.jpeg'
      ]
    };
  },
  methods: {
    openModal(image) {
      this.selectedImage = image;
      this.modalOpen = true;
    },
    closeModal() {
      this.modalOpen = false;
      this.selectedImage = '';
    }
  }
};
</script>

<style scoped>
.container {
  align-items: flex-start;
  display: flex;
  min-height: 100%;
  justify-content: center;
  padding: 64px 24px;
}

.card-grid {
  display: grid;
  grid-column-gap: 24px;
  grid-row-gap: 24px;
  max-width: 1200px;
  width: 100%;
}

@media(min-width: 540px) {
  .card-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media(min-width: 960px) {
  .card-grid {
    grid-template-columns: repeat(4, 1fr);
  }
}

.card {
  position: relative;
  cursor: zoom-in;
}

.card:before {
  content: '';
  display: block;
  padding-bottom: 150%;
  width: 100%;
}

.background {
  background-position: center;
  background-size: cover;
  bottom: 0;
  filter: brightness(0.75) saturate(1.2) contrast(0.85);
  left: 0;
  position: absolute;
  right: 0;
  top: 0;
  transition: filter 200ms linear, transform 200ms linear;

}

.card:hover .background {
  transform: scale(1.05);
  filter: none;
}

.card-grid:hover>.card:not(:hover) .background {
  filter: brightness(0.6) saturate(1) contrast(1.2) blur(5px);
}

.card-grid:hover>.card:not(:hover) .content {
  filter: brightness(0.8) blur(2px);
}

/* Modal */
.modal-overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.8);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 1000;
}

.modal-content {
  position: relative;
  background-color: black;
  padding: 10px;
  max-width: 90%;
  max-height: 90%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.modal-content img {
  max-width: 100%;
  max-height: 100%;
}

.modal-image {
  width: 100%;
  height: 100%;
  object-fit: contain;
  /* Mantiene le proporzioni originali senza deformare l'immagine */
  object-position: center;
}

.close-button {
  position: absolute;
  top: 10px;
  right: 10px;
  background-color: transparent;
  color: red;
  border: none;
  font-size: 50px;
  cursor: zoom-out;
}
</style>