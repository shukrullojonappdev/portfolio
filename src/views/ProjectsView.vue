<script setup lang="ts">
import ProjectItem from '../components/ProjectItem.vue'
import img1 from '../assets/screencapture-diplom-ishi-admin-firebaseapp-home-dashboard-2023-08-05-08_58_41-min.png'
import img2 from '../assets/screencapture-shollp-netlify-app-2023-08-05-08_54_39-min.png'
import img3 from '../assets/screencapture-shscoot-netlify-app-2023-08-05-08_56_05-min.png'
import img4 from '../assets/screencapture-soft-lebkuchen-37c5ed-netlify-app-2023-08-05-08_55_22-min.png'
import img5 from '../assets/screencapture-stellar-chebakia-1aa062-netlify-app-2023-08-05-08_56_35-min.png'
import img6 from '../assets/screencapture-ummonsuvi-web-app-2023-08-05-08_58_27-min.png'
</script>

<template>
  <div class="projects">
    <div class="shadow"></div>
    <div class="grid">
      <ProjectItem :imgsrc="img1" />
      <ProjectItem :imgsrc="img2" />
      <ProjectItem :imgsrc="img3" />
      <ProjectItem :imgsrc="img4" />
      <ProjectItem :imgsrc="img5" />
      <ProjectItem :imgsrc="img6" />
    </div>
    <div class="shadow"></div>
  </div>
</template>

<style scoped>
.grid {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin-top: 30px;
}

@media (min-width: 700px) {
  .grid {
    display: grid;
    grid-template-columns: 280px 280px;
    grid-gap: 15px;
  }

  .shadow:first-child {
    top: 30px;
  }
}

@media (min-width: 1200px) {
  .projects {
    position: relative;
  }
  .grid {
    max-height: 600px;
    overflow-y: auto;
    padding: 30px 0;
    display: grid;
    grid-template-columns: 280px 280px;
    grid-template-rows: 200px 200px 200px;
    grid-gap: 15px;
  }

  .grid::-webkit-scrollbar {
    display: none;
  }
  .shadow {
    position: absolute;
    right: 0;
    left: 0;
    height: 30px;
    background: rgb(2, 0, 36);
    background: linear-gradient(
      to bottom,
      #181818,
      rgba(24, 24, 24, 0.5) 50%,
      rgba(0, 212, 255, 0) 100%
    );
  }

  .shadow:last-child {
    bottom: 0;
    transform: rotate(180deg);
  }
}
</style>
