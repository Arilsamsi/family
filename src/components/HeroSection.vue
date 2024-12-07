<template>
  <section class="py-5 text-center bg-white position-relative">
    <div class="container">
      <h1 class="fw-bold mb-4 mt-4">Welcome to Our Family</h1>
      <p class="lead text-muted mb-5">Cherishing moments together as a family</p>
      <div class="position-relative">
        <button id="loveButton" class="btn btn-dark btn-lg" @click="emitParticles">
          Share the Love
        </button>
        <div id="tsparticles" style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></div>
      </div>
    </div>
    <div class="moving-photos mt-5">
      <div class="photo-track">
        <div class="photo-wrapper">
          <img v-for="n in 12" :key="`photo-${n}`" src="../assets/WhatsApp Image 2024-12-07 at 10.34.17.jpeg" class="photo rounded" alt="Family Photo" />
          <img v-for="n in 12" :key="`photo-duplicate-${n}`" src="../assets/WhatsApp Image 2024-12-07 at 10.34.17.jpeg" class="photo rounded" alt="Family Photo Duplicate" />
        </div>
      </div>
      <div class="photo-track reverse">
        <div class="photo-wrapper">
          <img v-for="n in 12" :key="`photo-${n}`" src="../assets/WhatsApp Image 2024-12-07 at 10.34.17.jpeg" class="photo rounded" alt="Family Photo" />
          <img v-for="n in 12" :key="`photo-duplicate-${n}`" src="../assets/WhatsApp Image 2024-12-07 at 10.34.17.jpeg" class="photo rounded" alt="Family Photo Duplicate" />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import { loadFull } from "tsparticles"; 
import { tsParticles } from "tsparticles-engine"; 

export default {
  methods: {
    async emitParticles() {

      await loadFull(tsParticles);

      tsParticles.load("tsparticles", {
        fullScreen: {
          enable: false, 
        },
        particles: {
          number: { value: 30 }, 
          shape: {
            type: "heart", 
          },
          size: {
            value: 10, 
          },
          move: {
            enable: true,
            speed: 5, 
            direction: "top", 
            outModes: {
              default: "out", 
            },
          },
        },
        interactivity: {
          events: {
            onclick: { enable: true, mode: "push" },
          },
        },
        detectRetina: true,
      });
    },
  },
};
</script>

<style scoped>
h1 {
  font-size: 2.5rem;
}

.moving-photos {
  overflow: hidden;
  position: relative;
  width: 100%;
  background: #f8f9fa;
  padding: 20px 0;
  border-radius: 10px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
}

.photo-track {
  display: flex;
  margin-top: 5px;
  animation: movePhotosRight 44s linear infinite; 
}

.photo-track.reverse {
  animation: movePhotosLeft 44s linear infinite; 
}

.photo-wrapper {
  display: flex;
  width: 100%; 
}

.photo {
  width: 150px;
  height: 150px;
  object-fit: cover;
  border: 3px solid #fff;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
  border-radius: 50%;
  margin: 0 10px; 
}

@keyframes movePhotosRight {
  0% {
    transform: translateX(0);
  }
  100% {
    transform: translateX(-100%); 
  }
}

@keyframes movePhotosLeft {
  0% {
    transform: translateX(-100%);
  }
  100% {
    transform: translateX(0); 
  }
}
</style>
