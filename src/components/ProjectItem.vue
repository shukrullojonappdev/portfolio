<script lang="ts" setup>
defineProps({
  imgsrc: String
})
</script>

<template>
  <div class="card">
    <img :src="imgsrc" alt="img" />
  </div>
</template>

<style scoped>
.card {
  height: 200px;
  width: 280px;
  margin-bottom: 15px;
  border-radius: 20px;
  overflow: hidden;
  box-shadow: 0px 0px 10px rgba(255, 255, 255, 0.3);
  position: relative;
}

img {
  object-fit: cover;
  width: 100%;
  height: 100%;
  transition-duration: 300ms;
}

img:hover {
  height: 150%;
}

@media (min-width: 700px) {
  .card {
    margin: 0;
  }
}

@media (min-width: 1200px) {
  .card {
    height: 100%;
    width: 100%;
  }
}
</style>
